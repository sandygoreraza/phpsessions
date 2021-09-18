# phpsessions
How to allow php sessions to carry over to subdomains


Note :

l had a challenge of figuring out how to use same session variable from main domain to subdomains. The solution is that you need to reference or in simple terms use same php.ini for main domain and subdomain and make sure the save path for sessions i.e <b>session.save_path</b> 
needs to be the same to share sessions.

and include the following code in your main singleton script on both domain and subdomains : 

<b>ini_set('session.cookie_domain', '.example.com' )</b>; 

replace example.com with your main domain name.
