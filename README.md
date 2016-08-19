# Escc.Web.SecurityConfig

Configuration settings to apply client-side security protections to a website running over TLS:

* Sets the `X-Frame-Options` HTTP header to `SAMEORIGIN` to block click-jacking attempts
* Sets the `X-XSS-Protection` HTTP header to `1; mode=block` to enable browsers' XSS built-in protection
* Sets the `X-Content-Type-Options` HTTP header to `nosniff` to require MIME types to be specified correctly
* Sets the `Strict-Transport-Security` HTTP header to a `max-age` of 1 year, meaning **your site can only be requested over HTTPS**
* Removes the unnecessary `X-Powered-By` HTTP header 
* **Locks down all client-side resources by default** using a content security policy, as a starting point for building a policy for your site. 

Test your site with at [securityheaders.io](https://securityheaders.io/) to find out more about how these settings protect your site.

## NuGet package

The NuGet package is created using the [NuBuild](https://github.com/bspell1/NuBuild) extension for Visual Studio.