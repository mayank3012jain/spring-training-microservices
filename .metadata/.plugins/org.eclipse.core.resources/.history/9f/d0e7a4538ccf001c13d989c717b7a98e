package com.cisco.training.ui;

import java.util.Scanner;

import com.cisco.training.domain.Product;
import com.cisco.training.service.ProductService;

public class ProductConsoleUI {
	
	ProductService service; // = new ProductServiceImpl();
	
	public void setService(ProductService service) {
		this.service = service;
	}
	
	public void createProductWithUI() {
		Scanner kb = new Scanner(System.in);
		
		System.out.println("Enter name: ");
		String name = kb.nextLine();
		
		System.out.println("Enter price: ");
		float price = Float.parseFloat(kb.nextLine());
		
		System.out.println("Enter QoH: ");
		int qoh = Integer.parseInt(kb.nextLine());
		
		Product p = new Product(name, price, qoh);
		int id = service.addNewProduct(p);
		System.out.println("Added Product with Id: "+id);
	}

}
