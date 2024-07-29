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

You can see the minified code inside the web console'sources by inspecting the website, the code is minified, obfuscated and compressed and you can make it readable with the pretty print button.


# Ressources
<!-- Images list -->

[xssAttackInsideInnerHtml]: ../../../assets/images/react_innerhtml_image_1.png
[propsCrafted]: ../../../assets/images/react_inner_html_props_crafted.png

## Glossary

**Minified**
> Focuses on reducing file size by removing unnecessary characters.

**Obfuscated**
> Focuses on making code harder to understand while preserving functionality.
**Compressed**
> Focuses on reducing file size through encoding techniques