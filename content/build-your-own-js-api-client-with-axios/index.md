---
title: "Build your own js api client with axios"
description: "Grafana TODO"
date: "2020-05-12T09:01:36.147Z"
categories: []
published: false
---

  

Grafana TODO

[**Dashboard HTTP API**  
_The identifier (id) of a dashboard is an auto-incrementing numeric value and is only unique per Grafana install. The…_grafana.com](https://grafana.com/docs/grafana/latest/http_api/dashboard/ "https://grafana.com/docs/grafana/latest/http_api/dashboard/")[](https://grafana.com/docs/grafana/latest/http_api/dashboard/)

[**Grafana**  
_If you're seeing this Grafana has failed to load its application files 1. This could be caused by your reverse proxy…_play.grafana.org](https://play.grafana.org/dashboards "https://play.grafana.org/dashboards")[](https://play.grafana.org/dashboards)

[**OpenAPI-GUI v3.0.0**  
_Edit description_mermade.github.io](https://mermade.github.io/openapi-gui/ "https://mermade.github.io/openapi-gui/")[](https://mermade.github.io/openapi-gui/)

[**OpenAPI Generator · Generate clients, servers, and documentation from OpenAPI 2.0/3.x documents**  
_The following generators are available:_openapi-generator.tech](https://openapi-generator.tech/docs/generators#client-generators "https://openapi-generator.tech/docs/generators#client-generators")[](https://openapi-generator.tech/docs/generators#client-generators)

  

How to build simple http api client

-   Flow (img) Do you really need to build it? (if api is external) - (do you need to have clients for a lot of languages?)
-   option 1 — favorite client library 
-   try to find existing client library for you language
-   try to find swagger for you client
-   find docs
-   timeouts (read/write)
-   allow to customize (request/response logs/…)
-   allow to create different instances
-   example — grafana-api-node-client/grafana-api-js-client
-   option 2 swagger
-   example — grafana 
-   example — aliseeks
-   example — shopify client  
    \- Java?  
    \- JavaScript / NoseJs?  
    \- PHP
-   [https://blog.bearer.sh/api-client-library-node-js/](https://blog.bearer.sh/api-client-library-node-js/)
-   [https://blog.logrocket.com/how-to-make-http-requests-like-a-pro-with-axios/](https://blog.logrocket.com/how-to-make-http-requests-like-a-pro-with-axios/)
-   [https://github.com/m0nhawk/grafana\_api](https://github.com/m0nhawk/grafana_api)
-   Make it simple — don’t add additional non-related logic to it. Will be easier to use for others

![](./asset-1.png)
