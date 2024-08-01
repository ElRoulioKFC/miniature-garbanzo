# React attacks 

## XSS Cross site scripting

Malicisous users are trying to launch script in our site.



### InnerHTML

#### Setup by the dev
Attackers uses the innerhtml to setup malicious code inside our html balise.

Example: wysiwig inside a comment that allow user to edit the source as an html comment. 
```html
Try these <b>3-ingredient cookies</b>! They’re <i>amazing</i>. <img src="nonexistent.png" onerror="alert('this script is launched by the site');" /> 
```
The image doesn't exist and the onerror attribute is used by the website => hacker can use this to inject their own code.
![schemaSummarize][xssAttackInsideInnerHtml]

#### propsInput object crafterd by the attacker

Howerver even when the dangerouslySetInnerHTML property isn't in the original props, an attacker can craft an propsInput.
![schemaSummarize][propsCrafted]

#### Prevent

Whenever possible avoid using dangerouslySetInnerHTML property and if you do, exercise extreme caution and never assign the unsanitized user input to its value.

When using a props object, make sure it is sanitiezd and doesn't contain any contaminated content.

#### Key takeaways

The dangerouslySetInnerHTML property is React’s replacement for setting the innerHTML property of an HTML element. This property contains HTML markup of the element, and it is used to render HTML content.

This property is not escaped or sanitized automatically by React. As a result, populating it with unsanitized user input exposes the application to XSS attacks.

Even when it is not used in the application's code, an attacker can insert the DangerouslySetInnerHTML property into a props object and use it to perform XSS attacks. To prevent such cases, make sure the props object is fully sanitized.



### sensitive datas

Any information, even partial, that must be protected against unhauthorized access.

#### Sensitive data in client side code
Hard coded variable can be easily inspected. Most of the time these datas aren't relevant for end-users and are kept in the client-side code because of wrong security design.

You can see the minified code inside the web console'sources by inspecting the website, the code is [minified](#minified), [obfuscated](#obfuscated), and [compressed](#compressed). You can make it readable with the pretty print button.

The attackers then can search for valuable keywords, like IdentityPoolId, to gather the api's key.

Even when the code is compiled with a build version the variables remain unchanged.

#### Key takeaways

Remember that client-side variables can be read and manipulated by literally anyone. Hence, sensitive data should never be kept in client-side variables.

Using the basics npm run build / yarn build command, the code is bundled, minified, and compressed. Thus, it would be harder for an adversary to understand the flow of the application and find security holes.

You can also uses Obfuscation Tools eto make the code even less readable.

Use SAST Tools (Static Application Security Testing) to find security vulnerabilities in the application source code in general and sensitive data exposure.

Be carefull with hard-coded variables. They are still readable by users.

#### Prevent

The sensitive data storing inside client-side code is incorrect design.

You can also uses Obfuscation Tools eto make the code even less readable.


### Cross-site Request forgery

CSFR are attacks that causes an authenticated victim user to unknowingly submit a malicious request. There are no built-in react protection against this type of attacks.

If there are no protection against CSFR attacks, the attacker can make a button / link that causes the victim to acts on another site.

You can then trap the other user to access to a malicious webpage that will access the initial webpage. <link to do> See the html example of attacks.

#### Conditions

An CSFR attack is can only be succesful if theses criterias are met:
    + The victim is logged into the vulnerable application
    + The critical action is performed in a single step using a GET or POST HTTP request.
    + There are no protection against CSFR attack.
    + Existing security controls, like same origin policy, are neglected.


#### Prevent

Use authenticated cookies and verification when making important actions in the site

Add CSFR token to the API request, it will first receive the csfr token from the cookie and add it to the header.

Use SameSite cookies to prevent the browser from sending the cookies to the other site. The SameSite attribute specifies whether the cookie is sent with cross-site requests.

#### Key takeaways

CSRF attacks exploit the trust that a site has in the user's browser. They can be prevented by using security tokens or by verifying the origin of the request.

CSRF attacks are more likely to succeed when the user is authenticated and the action is performed in a single step.

A CSRF attack can only be successful if the application is vulnerable to it. It is crucial to implement security measures that prevent CSRF attacks.

The SameSite attribute can be used to prevent the browser from sending cookies in cross-site requests, which can help mitigate CSRF attacks

The implementation of CSRF protection should rely on a same-origin policy in browsers. Meaning, only Javascript residing on the exact same origin domain can access the cookie value and set custom headers.

The React-based application implements only the client-side part of the CSRF protection. The server should also set and check the CSRF tokens. 

# Ressources
<!-- Images list -->

[xssAttackInsideInnerHtml]: ../../../assets/images/react_innerhtml_image_1.png
[propsCrafted]: ../../../assets/images/react_inner_html_props_crafted.png

## Glossary

### Minified (code)
> Focuses on reducing file size by removing unnecessary characters.

### Obfuscated (code)
> Focuses on making code harder to understand while preserving functionality.

### Compressed (code)
> Focuses on reducing file size through encoding techniques.