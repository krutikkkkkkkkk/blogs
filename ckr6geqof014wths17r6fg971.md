## Setting Up Custom 404 Error Page

### What does HTTP 404 mean?

The HTTP 404, 404 Not Found, 404, 404 Error, Page Not Found or File Not Found error message is a Hypertext Transfer Protocol standard response code, in computer network communications, to indicate that the browser was able to communicate with a given server, but the server could not find what was requested. 

Want to Know More About HTTP Response codes Checkout.

https://ayushirawat.com/http-status-codes-that-you-must-know

<hr>

**The Default 404 error pages are not good looking and don't have any type of navigations**

Following are some methods you can use to auto-redirect to a custom error page.


- ** Website Running on Apache webserver**


1. Create a custom webpage for 404 error and name it 404.html

2. Create a file name `.htaccess`

File content: ErrorDocument {error_code}  {custom file path}
```
ErrorDocument 404 /404.html 
``` 
OR

```
ErrorDocument 404 https://yourwebsite.com/404.html 
```

Now the site will redirect to 404.html whenever the user gets a 404 HTTP response or browse the wrong URL path on your website.

**Here are some hosting services that run on Apache webserver**

<table>
<tbody>
  <tr>
    <td>Hostinger</td>
    <td>Heroku</td>
    <td>GoDaddy</td>
  </tr>
  <tr>
    <td>Netlify</td>
    <td>BlueHost</td>
    <td>1&amp;1</td>
  </tr>
  <tr>
    <td>Cloudways</td>
    <td>SiteGround</td>
    <td>HostGator</td>
  </tr>
</tbody>
</table>

<hr>

- ** Website Hosted on Vercel.com**


1. Create a custom webpage for 404 error and name it 404.html

2. Create a file name `vercel.json`

File content:
```
{
  "routes": [
    { "handle": "filesystem" },
    { "src": "/(.*)", "status": 404, "dest": "/404.html" }
  ]
}
```

Read more at official docs: https://vercel.com/guides/custom-404-page


<hr>


- **Website hosted on Github Page**

    *The simplest so far*



1. Create a custom webpage for 404 error and name it 404.html

2. Add this file to your repository

3. Done 

<hr>

- **Website running on Heroku**

For a PHP app hosted on Heroku follow the same method as of Apache Server

OR

1. Create a custom webpage for 404 error and name it 404.html

2. Run this command on Heroku CLI

```
heroku config:set \ 
ERROR_PAGE_URL=//yourwebsite.com/public/404.html
```

Read more at official docs: https://devcenter.heroku.com/articles/error-pages

<hr>

*Note: Make sure the 404.html is present in your root directory with index.html*

** Video Tutorial [Apache Server]** : https://www.youtube.com/watch?v=QkB5ZxeYaJQ&t


### Social Links

[Instagram](https://instagram.com/reboot13_dev) |
[Youtube](https://youtube.com/krutikraut)  |
[Twitter](https://twitter.com/reboot13_dev) |
[Codepen](https://codepen.io/reboot13)


<center> **ThankYou **</center>









