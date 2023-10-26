Use this configuration to force HTTPS in [[Spring_Boot]]:
\
@Configuration
public class SecurityConfiguration extends WebSecurityConfigurerAdapter {

@Override
	protected void configure(HttpSecurity http) throws Exception {
		http.requiresChannel().anyRequest().requiresSecure();
	}
}
By default [[Spring_Boot]] will run over https and use port 8080 in the cloud, so you can set the configuration up like this instead so itll only look for exported protoheader:
\
@Configuration
public class SecurityConfiguration extends WebSecurityConfigurerAdapter {

@Override
	protected void configure(HttpSecurity http) throws Exception {
		http.requiresChannel()
		.requiresMatchers(r -> r.getHeader("X-Forwarded-Proto") != null)
		.requiresSecure();
	}
}

This is mainly useful for when Heroku or other cloud providers they will send this header when there needs to be https.