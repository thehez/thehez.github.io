---
layout: post
title: Understanding the OWASP Top 10 (Part One)
date: 2023-12-12 12:22
categories: [Blog, Security]
tags: [pentesting, appsec, security] 
---

## Unwrapping the 2021 OWASP Top 10: Why the Classics Still Matter

The OWASP Top 10 is a cybersecurity checklist that identifies the most critical web application security risks. Despite the influx of flashy new threats in the wild, the 2021 edition of the Top 10 still remains relevant as it focuses on widespread, impactful vulnerabilities that consistently jeopardize web apps. 

Anticipating an update to the Top 10 as we approach the end of 2023🎄✨, I want to explore these enduring vulnerabilities, focusing on why they remain relevant and how we can implement practical solutions to secure our applications for the future.

### First up, what is OWASP?
The Open Web/Worldwide Application Security Project, commonly known as OWASP, is a non-profit foundation dedicated to enhancing the security of software applications worldwide. 

Founded on the principles of collaboration and knowledge sharing, the organization actively develops and maintains a diverse array of projects, tools and services aimed at enhancing the security of web, API, and mobile applications. In this 2 part series we are going to focus on argubly their most famous project, the [OWASP Top 10](https://owasp.org/www-project-top-ten/).

### Why OWASP Top 10?
![Why is OWASP](/assets/img/OWASP-top-10/Why-is-OWASP.png){: .right }

The OWASP Top 10 stands as a fundamental resource for developers, penetration testers, DevSecOps practitioners, security engineers, and all stakeholders engaged in the Software Development Life Cycle (SDLC) of applications.

Serving as a widely acknowledged guide in the cybersecurity community, the document sheds light on the most critical, pervasive, or commonly exploited security risks and vulnerabilities inherent in web applications.

Collaboratively curated with distinguished experts in the cybersecurity realm, the guidance offered by OWASP is a reliable roadmap for crafting a comprehensive security strategy during the development of websites and apps. 

While typically receiving updates every couple of years, the OWASP Top 10 has held steady since 2021. Anticipating an update in 2024 or 2025, the present reliance on the 2021 list underscores the enduring relevance of the identified vulnerabilities. 

### The Top 10

#### A10:2021 – Server-Side Request Forgery (SSRF)

Server-Side Request Forgery (SSRF) was a new addition to the top 10 in 2021. According to OWASP, the data shows a low incidence rate but an increased alarm from security members within the field. This is likely due to the increased impact of succesful SSRF attacks within cloud hosted environments, which have become more popular due to rapid migrations of applications to the public cloud. 

To see just how damaging this vulnerability can be, one just has to look to the now infamous Capital One attack, in which a malicious actor leveraged an SSRF exploit against AWS services to steal over 30GB of Capital One credit application data, affecting over a million users.

So, what is it?

SSRF is a type of security vulnerability that occurs when an attacker can influence or manipulate a server to make requests to other internal resources or external services. In short, the attacker typically tricks the server into making requests to unintended destinations, often causing unauthorized access to internal systems or sensitive services.

Consider the following:

```python
from flask import Flask, request
import requests

app = Flask(__name__)

@app.route('/fetch_data', methods=['GET'])
def fetch_data():
    url = request.args.get('url')

    response = requests.get(url)

    return response.text

if __name__ == '__main__':
    app.run(debug=True)
```

In the above code snippet, we have a simple Flask web application with an exposed endpoint ***/fetch_data*** that takes a URL parameter ***('url')***. The value provided to this parameter is then directly used in the subsequent ***requests.get()*** function to make an HTTP GET request. 

Although this may seem innocent enough, the functionality hides a significant vulnerability as an attacker can provide any value they like to the ***url*** parameter. Without proper validation or filtering, malicious actors could abuse this functionality; manipulating the url parameter to point to internal resources, potentially causing the server to make unauthorized requests to sensitive internal APIs or files. 

Lets see this in action



### Further Reading

Further information on the Capital One attack can be found in the blog post by [Krebs on Securty - Capital One hack ](https://krebsonsecurity.com/2019/08/what-we-can-learn-from-the-capital-one-hack/).

For more information about the OWASP Foundation, including cheatsheets and local chapters, head over to 