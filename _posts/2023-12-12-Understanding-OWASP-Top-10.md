---
layout: post
title: Understanding the OWASP Top 10 (Part One)
date: 2023-12-12 12:22
categories: [Blog, Security]
tags: [pentesting, appsec, security] 
---

## Unwrapping the OWASP Top 10 : Why the Classics Still Matter

The OWASP Top 10 is a cybersecurity checklist that identifies the most critical web application security risks. Despite the influx of flashy new threats in the wild, the Top 10 remains relevant because it focuses on widespread impactful vulnerabilities that consistently jeopardize web apps. 

As we approach the end of 2023🎄✨, I want to explore these enduring vulnerabilities, focusing on why they remain relevant and how we can implement practical solutions to secure our applications for the future.

### First up, what is OWASP?
The Open Web/Worldwide Application Security Project, commonly known as OWASP, is a non-profit foundation dedicated to enhancing the security of software applications worldwide. 

Founded on the principles of collaboration and knowledge sharing, OWASP has evolved into a beacon for enthusiasts, developers, and cybersecurity professionals alike. The organization actively develops and maintains a diverse array of projects aimed at enhancing the security and proficiency of web, API, and mobile applications. These initiatives include;
 
 The [Firewall Core Rulesets](https://owasp.org/www-project-modsecurity-core-rule-set/) 
 : commonly used in cloud environments and with managed Web Application Firewalls (WAFs).

 The [OWASP Juice Shop](https://owasp.org/www-project-juice-shop/)
 : a go-to-resource for practicing web app testing tools and techniques.
 
 And the [Web Security Testing Guide](https://owasp.org/www-project-web-security-testing-guide/)
 : a comprehensive guide for security professionals testing web applications and services.

In this 2 part series we are going to focus on argubly their most famous project, the [OWASP Top 10](https://owasp.org/www-project-top-ten/).

### Why OWASP Top 10?
![Why is OWASP](/assets/img/OWASP-top-10/Why-is-OWASP.png){: .right }

The OWASP Top 10 serves as a foundational resource for developers and those involved in web application security, offering a widely accepted guide on the most critical security risks faced by web applications. This standard awareness document represents a collective agreement within the cybersecurity community, highlighting key vulnerabilities that demand attention.

Typically updated every three years, the OWASP Top 10 has remained unchanged since 2021. Although an update is anticipated in the next couple of years, the current reliance on the 2021 list underscores the persistent relevance of the identified vulnerabilities. The compilation process involves comprehensive data collection from over 200,000 organizations and insights gathered through surveys of industry professionals.

While the prospect of a 2023 update looms, the importance of the 2021 list cannot be understated. These vulnerabilities continue to pose significant threats in web development and security. It is imperative for professionals in these domains to remain vigilant and well-informed about these risks, as they navigate the evolving landscape of web application security.


### Further Reading

For more information about the OWASP Foundation, including cheatsheets and local chapters, head over to t