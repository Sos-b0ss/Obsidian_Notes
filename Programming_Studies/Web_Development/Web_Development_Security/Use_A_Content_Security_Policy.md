This essentially specifies that your front end can only access certain things, and do certain things, like run pre specified javascript. It can also even lock down whether or not javascript can perform an eval.
\
With Default Spring Security Headers:
\
Cache-Control: no-cache, no-store, max-age=0, must-revalidate
Pragma: no-cache
Expires: 0
X-Content-Type-Options: nosniff
Strict-Transport-Security: max-age=31546000; includeSubDomains
X-Frame-Options: DENY
X-XSS-Protection: 1; mode=block
\
but nice thing you can do with [[Spring_Security]] is if you want to enable a [[CSP]] header in spring boot you can add this config:
\
@EnableWebSecurity
public class SecurityConfiguration extends WebSecurityConfigurerAdapter {
	@Override
	protected void configure(HttpSecurity http) throws Exeption {
		.contentSecurityPolicy("script-src 'self' " +
			"https://trustedscripts.example.com; " +
			"object-src https://trustedplugins.example.com; " +
			"report-uri /csp-report-endpoint/");
	}
}
\
Another feature of this is that if springboot was configured properly you can go to the site: https://securityheaders.com to test your app and youll get like an A+ if its all covered.