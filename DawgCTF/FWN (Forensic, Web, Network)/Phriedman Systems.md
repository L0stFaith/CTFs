# Phriedman Systems (250)

<blockquote> 
We want access to the CEO's secure data. Log in to their website using the CEO's account. https://phriedmansystems.onrender.com/
<br></br>
Hints:

<br>• This is primarily a Recon challenge. </br>
• There is NO password cracking, brute force, or password guessing required.
<br>• There is NO steganography of any sort required. </br>
• The onrender.com website is just used for hosting. Attacking Render is not a part of the challenge; do not attack Render or attempt to break into the backend.
<br>• You don't need to use anything on the Internet at all apart from phriedmansystems.onrender.com.</br>

Author: nb 
</blockquote>

# Solution

As you can see from the text of the task we shouldn't try to guess or hack something. We also can see that all valuable information exists only on this site. So, lets begin...

<br>First, pay attention to the category of this challenge. It's FWN (Forensic, Web and Network). Based on it, we will use the following methods. </br>
1. When i see task from Web category i always like to check out <code>/robots.txt</code> directory.

Excellent! We found login page.

<pre>User-agent: *
Allow: /
Disallow: /login.html</pre>

Let's check this page.

<p align="center">
  <img src="https://user-images.githubusercontent.com/79190893/117558742-350ba900-b0c3-11eb-8ec1-53d626f55f31.PNG">
</p>

As we can see, first we need to find out the SEO's login. 

2. Let's explore all pages. 

The next hint we can find on the tabs <code>"Employees"</code> and <code>"Careers"</code>. On both tabs, we can find the e-mail of employees. 

On the <code>"Employees"</code>: <code>Rob Fiddson - Mechanical Engineer: rfiddson@phriedmansystems</code> 
<br>On the <code>"Careers"</code>: <code>Stephanie Leaver - Director of HR: sleaver@phriedman.xyz</code></br>

Based on this, we can see that the login is the first letter of the name + last name! Thus, the SEO login: <code>csmith</code>
Let's check it out. Correct!

<p align="center">
  <img src="https://user-images.githubusercontent.com/79190893/117559070-8c127d80-b0c5-11eb-8794-740664efd230.png">
</p>

3. It remains to find out the password. 

Unfortunately, having carefully researched the entire site, I could not find information that would be useful... The only thing left is the phone number. Let's try to call!
<br>IT'S WORKING! We got an answer!</br> 
The answering machine offers us a choice of menu options.
<br>Having used all the menu options, we can notice that the first option allows us to get more detailed information about the company. It may be useful!</br>
Under the fourth option we find technical support! Bingo! We can recover the password by login! Next, using the keyboard, we need to specify the login. 
<br><br>In the picture below, you can see an example of a keyboard: </br></br>

<p align="center">
  <img src="https://user-images.githubusercontent.com/79190893/117559349-e1e82500-b0c7-11eb-8b69-8f4ec017ac3e.jpg">
</p>

Using the numbers, enter the login. And at the end we add "#" for input: <code>222 222 7777 6 444 8 44 #</code>
<br><br>In response, we receive a warning that we can restore this account only by correctly answering the question.</br></br>
As an answer, we need to enter the favorite city of the CEO. We got this information in the first menu option. It's <code>Albany</code>.
<br><br>Using the keyboard, enter the name of the city. If we see "two letters on one number", then we need to add "0". And at the end we add "#" for input: <code>2 555 22 0 2 66 999 #</code> </br></br>
Password reset! New password: <code>monkey_alpaca_excellent_button_7435</code>

Log in to the site and get the flag: <code>DawgCTF{y0ur_c4ll_1s_v3ry_1mp0rt4nt_t0_u5}</code>
