#Authorization api with OAuth 2.0

## Table Of Content
[Intro](https://github.com/Team-manager-website/Portfolio/blob/main/Documents/Research/Authorization%20api%20with%20OAuth%202.0.md#intro)<br>
[What is OAuth 2.0]([https://github.com/Team-manager-website/Portfolio/blob/main/Documents/Research/Authorization%20api%20with%20OAuth%202.0.md#intro](https://github.com/Team-manager-website/Portfolio/blob/main/Documents/Research/Authorization%20api%20with%20OAuth%202.0.md#what-is-oauth-20))<br>
[Benefits and the drawbacks](https://github.com/Team-manager-website/Portfolio/blob/main/Documents/Research/Authorization%20api%20with%20OAuth%202.0.md#benefits-and-the-drawbacks)<br>
[How does OAuth 2.0 work](https://github.com/Team-manager-website/Portfolio/blob/main/Documents/Research/Authorization%20api%20with%20OAuth%202.0.md#how-does-oauth-20-work)<br>
[Sources](https://github.com/Team-manager-website/Portfolio/blob/main/Documents/Research/Authorization%20api%20with%20OAuth%202.0.md#sources)<br>

## Intro 
In this research document we are looking at authorization an api call with OAuth 2.0. I will take look at what the benefits and the drawbacks are for using OAuth 2.0. But the main thing we are going to explore is how I am going to implement OAuth 2.0 in my project.
In my project I use java for the back end and vue for the front-end so the research will be focus on those two languages. 
 
## What is OAuth 2.0
OAuth is standing for Open Authorization, it is a designed to allow a website or application to access resources that comes from other websites on behalf of a user. In 2012 it replaces OAuth 1.0, and it is now the standard for authorization. It provides authorization flows for applications. The service provides access and restricts actions of what the client can perform on recources on behalf of the user without sharing credentials.

### Benefits and the drawbacks
The benefits for using OAuth 2.0:
* The api is secured.
*	The access is realized via http/https.
*	There is a lot of information on the internet about it.
*	You can use it for almost any application.
*	It is a popular service.

### The drawbacks for using OAuth 2.0:
*	There is no common format, this result that each service requires its own implementation.
*	If the token gets closed it has no access for a while
*	The data can be shared on many ways without knowing it.

 
## How does OAuth 2.0 work
In the following steps I will show how the process of OAuth works. 
1. The client request authorization from the resource owner.
2. The resource owner gives authorization grant to the client. 
3. The client requests an access token through identity verification.
4. The authorization server verifies authorization grant and if it is valid, it will send an access token back.
5. Now the client requests a protected resource from the provider with the access token.
6. If the access token is valid, it serves the request.

 
 
## Sources
Auth0: https://auth0.com/intro-to-iam/what-is-oauth-2 
Stfalcon: https://stfalcon.com/en/blog/post/oauth-2.0 
