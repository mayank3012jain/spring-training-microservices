package com.cisco.training.service;

import java.util.List;
import java.util.Optional;

import javax.annotation.PostConstruct;

import org.springframework.beans.factory.annotation.Autowired;
import org.springframework.beans.factory.annotation.Qualifier;
import org.springframework.stereotype.Service;

import com.cisco.training.dal.ProductDAO;
import com.cisco.training.domain.Product;

//@Service("SpecialService")
public class ProductServiceSpecialImpl implements ProductService{
	
	@Autowired
	@Qualifier("SpecialDao")
	ProductDAO dao;
	
	@PostConstruct
	public void init(){
		
	}

	@Override
	public int addNewProduct(Product toBeAdded) {
		// TODO Auto-generated method stub
		return 0;
	}

	@Override
	public void removeExisting(int id) {
		// TODO Auto-generated method stub
		
	}

	@Override
	public Optional<Product> findById(int id) {
		// TODO Auto-generated method stub
		return null;
	}

	@Override
	public List<Product> findAll() {
		// TODO Auto-generated method stub
		return null;
	}

}
