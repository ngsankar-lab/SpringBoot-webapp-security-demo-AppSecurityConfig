# SpringBoot-webapp-security-demo-AppSecurityConfig
Spring Boot webapp security with AppSecurity Config

What is it?
----------

Created an AppSecurityConfig class by extending WebSecurityConfigurerAdapter
override the userDetailsService() method by adding the user to it like below
protected UserDetailsService userDetailsService() {

		List<UserDetails> users=new ArrayList<>();
		users.add(User.withDefaultPasswordEncoder().username("ngs").password("ngs").roles("USER").build());
		
		return new InMemoryUserDetailsManager(users);
}

Annotations used:
----------------
@Configuration - to declare the class as configuration
@EnableWebSeurity
@Bean
@Override

