package com.packt.webstore.config;

 import org.springframework.context.annotation.Bean;
 import org.springframework.context.annotation.ComponentScan;
 import org.springframework.context.annotation.Configuration;
 import org.springframework.web.servlet.config.annotation.DefaultServletHandlerConfigurer;
 import org.springframework.web.servlet.config.annotation.EnableWebMvc;
import org.springframework.web.servlet.config.annotation.PathMatchConfigurer;
import org.springframework.web.servlet.config.annotation.WebMvcConfigurerAdapter;
 import org.springframework.web.servlet.view.InternalResourceViewResolver;
 import org.springframework.web.servlet.view.JstlView;
import org.springframework.web.util.UrlPathHelper;
 
 @Configuration     //This indicates that a class declares one or more @Bean methods
 
 @EnableWebMvc		// Adding this annotation to an @Configuration class imports some special Spring MVC configuration
 // also, needed to enable annotations such as @controller and @RequestMapping
 
 @ComponentScan("com.packt.webstore")    // This specifies the base packages to scan for annotated components (beans)
 
 public class WebApplicationContextConfig extends WebMvcConfigurerAdapter {
	 
	 @Override
	 public void configureDefaultServletHandling (DefaultServletHandlerConfigurer configurer) {
	 configurer.enable();
	 }
	 
	 @Override
	 public void configurePathMatch(PathMatchConfigurer configurer) {
	 
		 UrlPathHelper urlPathHelper = new UrlPathHelper();
		 urlPathHelper.setRemoveSemicolonContent(false);
		 
		 configurer.setUrlPathHelper(urlPathHelper);
	 }
	 
	 
	 
		 @Bean
		 public InternalResourceViewResolver getInternalResourceViewResolver() {
			 
			 InternalResourceViewResolver resolver = new InternalResourceViewResolver();
			 
			 resolver.setViewClass(JstlView.class);
			 
			 resolver.setPrefix("/WEB-INF/views/");
			 resolver.setSuffix(".jsp");
			 
			 return resolver;
		 }
	
		 
 }