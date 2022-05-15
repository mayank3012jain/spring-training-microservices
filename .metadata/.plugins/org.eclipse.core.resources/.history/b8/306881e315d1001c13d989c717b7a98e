package com.cisco.training;

import org.springframework.boot.SpringApplication;
import org.springframework.boot.autoconfigure.SpringBootApplication;
import org.springframework.context.ApplicationContext;
import org.springframework.data.jpa.repository.config.EnableJpaRepositories;

import com.cisco.training.dal.ProductDAOJpaImpl;
import com.cisco.training.ui.ProductConsoleUI;

@SpringBootApplication
//@EnableJpaRepositories
public class ProductAppApplication {

	public static void main(String[] args) {
		ApplicationContext springContainer = 
				SpringApplication.run(ProductAppApplication.class, args);
		
		ProductConsoleUI bean = springContainer.getBean(ProductConsoleUI.class);
		bean.createProductWithUI();
	}

}
