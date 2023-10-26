With spring security you have [[CSRF]] Protection in place by default with this configuration. 
\
@EnableWebSecurity
public class SecurityConfiguration extends WebSecurityConfigurerAdapter {
	@Override
	protected void configure(HttpSecurity http) throws Exeption {
		http
			.csrf()
			.csrfTokenRepository(
			CookieCsrfTokenRepository.withHttpOnlyFalse());
	}
}
\
If youre using a REST API then this configuration may want to be disabled, but if youre creating a javascript framework like with [[Angular]] or [[React]] and you want to have CSRF enabled itll have to enabled with the configuration above.
\
There is however a new solution called:
[[SameSite_Attribute]] that you can put on cookies to make SameSite Cookies
\
This communicates to the clients browser and thats all it can communicate with. The only downside is that this does as well prevent any 3rd party cookies which can be a whole other issue if your users are trying to access this site with information from another part of your app.