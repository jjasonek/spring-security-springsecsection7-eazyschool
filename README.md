# Udemy Course Spring Security Section7 - eazyschool
## spring version: 3.4.4


## Login Configurations for MVC or monolithic apps

In the initial phase the application uses the default spring Security Login page.
We want to use teh custom one.


### setting the custom login page 
After changing the formLogin() to display our custom login page, 
we get error: "ERR_TOO_MANY_REDIRECTS"
That's why we also add "/login/**" to permitAll() in authorizeHttpRequests(). 
This means all paths beginning with "/login/" are allowed to be accessed without authentication.


Now, using the "user" credentials on the login page, the application redirects me to home page. 
Byt I want the Dashboard page: http://localhost:8080/dashboard.
