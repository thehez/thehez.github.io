---
layout: post
title: Understanding the OWASP Top 10 (Part One)
date: 2023-12-12 12:22
categories: [Blog, Security]
tags: [pentesting, appsec, security] 
---

## Unwrapping the OWASP Top 10 : Why the Classics Still Matter

The OWASP Top 10 is a cybersecurity checklist that identifies the most critical web application security risks. Despite the influx of flashy new threats in the wild, the 2021 Top 10 edition still remains relevant because it focuses on widespread, impactful vulnerabilities that consistently jeopardize web apps. 

Anticipating an update to the Top 10 as we approach the end of 2023🎄✨, I want to explore these enduring vulnerabilities, focusing on why they remain relevant and how we can implement practical solutions to secure our applications for the future.

### First up, what is OWASP?
The Open Web/Worldwide Application Security Project, commonly known as OWASP, is a non-profit foundation dedicated to enhancing the security of software applications worldwide. 

Founded on the principles of collaboration and knowledge sharing, the organization actively develops and maintains a diverse array of projects, tools and services aimed at enhancing the security of web, API, and mobile applications. Some of the more well known of these initiatives include:
 
 [Firewall Core Rule Sets](https://owasp.org/www-project-modsecurity-core-rule-set/) 
 : commonly used in cloud environments and with managed Web Application Firewalls (WAFs), rulesets aim to protect web applications from a wide range of attacks, including those within the OWASP Top Ten :wink:, with a minimum of false alerts.

 [OWASP Juice Shop](https://owasp.org/www-project-juice-shop/)
 : a go-to-resource for app security professionals. The OWASP Juice Shop is a modern, realistic and intentionally insecure web application designed for the purpose of practicing and improving application security skills. 
 
 [Web Security Testing Guide](https://owasp.org/www-project-web-security-testing-guide/)
 : a comprehensive guide for security professionals testing web applications and services. 'Created by the collaborative efforts of cybersecurity professionals and dedicated volunteers, the WSTG provides a framework of best practices used by penetration testers and organizations all over the world.'

However, in this 2 part series we are going to focus on argubly their most famous project, the [OWASP Top 10](https://owasp.org/www-project-top-ten/).

### Why OWASP Top 10?
![Why is OWASP](/assets/img/OWASP-top-10/Why-is-OWASP.png){: .right }

The OWASP Top 10 stands as a fundamental resource embraced by developers, penetration testers, DevSecOps practitioners, security engineers, and all stakeholders engaged in the Software Development Life Cycle (SDLC) of applications. Serving as a widely acknowledged guide in the cybersecurity community, this document sheds light on the most critical, pervasive, or commonly exploited security risks and vulnerabilities inherent in web applications.

Collaboratively curated with distinguished experts in the cybersecurity realm, the guidance offered by OWASP is a reliable roadmap for crafting a comprehensive security strategy during the development of websites and apps. While typically receiving updates every three years, the OWASP Top 10 has held steady since 2021. Anticipating an update in 2024 or 2025, the present reliance on the 2021 list underscores the enduring relevance of the identified vulnerabilities. These threats persistently loom over web development and security, requiring the ongoing vigilance and informed awareness of professionals within the dynamic landscape of web application security.

### The Top 10

#### A10:2021 – Server-Side Request Forgery (SSRF)

Server-Side Request Forgery (SSRF) was a new addition to the top 10 in 2021. According to OWASP, the data shows a low incidence rate but an increased alarm from security members within the field. This is likely due to the increased impact of succesful SSRF attacks within cloud hosted environments due to rapid migrations of applications to the public cloud. One just has to look to the infamous Capital One attack which leveraged an SSRF exploit against AWS infrastructure, to see how dangerous this vulnerabilitiy can be. 

SSRF is a type of security vulnerability that occurs when an attacker can influence or manipulate the requests made by a web application to other internal resources or external services. In SSRF attacks, the attacker typically tricks the server into making requests to unintended destinations, often causing unauthorized access to internal systems or external services. 

...

### Further Reading

Further information on the Capital One attack can be found in the blog post by [Krebs on Securty ](https://krebsonsecurity.com/2019/08/what-we-can-learn-from-the-capital-one-hack/).

For more information about the OWASP Foundation, including cheatsheets and local chapters, head over to 