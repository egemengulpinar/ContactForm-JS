# Create Contact From - JavaScript
Only using with JavaScript and HTML, we can create a minimal contact form that we will use it everywhere.
It can implement easly to all web sites and blogs. Just following instructions and implement it on website correctly.



![Logo](https://www.linkpicture.com/q/contact_form_screenshot.png)




  

## Demo



![Alt Text](https://media.giphy.com/media/CC7Dr8AnXujxxexmJS/source.gif?cid=790b7611239b60dcba67c80fa2db550fe7de0e6bed5c241d&rid=source.gif&ct=g)
  
## Using & Run 

Clone the project

```bash
  git clone https://github.com/egemengulpinar/ContactFrom-JS.git
```


Open `Visual Studio Code` or similar code editor  and import `contact_form.html` file.
Now, it should to be configure with e-mail service. (I was used `EmailJS` service)

#### Configure EmailJS Service with Contact Form
First, open a new account on EmailJS

Integrate your e-mail account with EmailJS and authorize the options.

![Logo](https://www.linkpicture.com/q/contact_form_screenshot3.png)


You can personalized e-mail template in this tab. 
![Logo](https://www.linkpicture.com/q/contact_form_screenshot4.png)

I was used these template, when anyone fill the contact form, the messages reach to me with these format.
```
Name : {{ Your_Name }}

E-Mail Address : {{ Your_Email_Address }}

Telephone Number : {{ Your_Telephone_Number }}

Topic : {{ Topic }}

Message : {{ Your_Message }}
```


Then, in the `Integration` page, click `Browser` tab and copy the **<script> ... </script>** codes and paste 
your project(*In my contact form they are already included, 
just change **`"user_Yrsxxxxxxxxx"`*** information.

*On the below, they are listed your unique API keys. You can use these for another method.*
![Logo](https://www.linkpicture.com/q/contact_form_screenshot2.png)




`const serviceID` and `const templateID` should be enter from your EmailJS **Email Templates** and **Email Services** tabs information.


Finally, paste the **<script> ... </script>** codes to project(*In my contact form they are already included, just change **`"user_Yrsxxxxxxxx"`***)




```
<script>
   ...

   const serviceID = 'service_1715xxxx';
   const templateID = 'template_ahl7xxx';

   emailjs.sendForm(serviceID, templateID, this)
    .then(() => {
      btn.value = 'Send Email';
      alert('Message Send Succesfully, Thank You!');
    }, (err) => {
      btn.value = 'Send Email';
      alert(JSON.stringify(err));
    });
});
</script>

```
