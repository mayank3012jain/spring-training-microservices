package com.cisco.training.service;

import java.util.List;
import java.util.Optional;

import com.cisco.training.dal.ProductDAO;
import com.cisco.training.domain.Product;

public class ProductServiceImpl  implements ProductService{

	private static final int PRODUCT_MIN_VALUE = 10_000;


	private static final float PRODUCT_DELETION_THRESHOLD = 100_000;

	
	ProductDAO dao; // = new ProductDAOInMemImpl();
	
	public void setDao(ProductDAO dao) {
		this.dao = dao;
	}
	
	@Override
	public int addNewProduct(Product toBeAdded) {
		if(toBeAdded.getPrice() * toBeAdded.getQoh() < PRODUCT_MIN_VALUE) {
			throw new IllegalArgumentException("Min stock value expected to add is "+PRODUCT_MIN_VALUE+" , but was "+toBeAdded.getPrice() * toBeAdded.getQoh());
		}
		Product saved = dao.save(toBeAdded);
		return saved.getId();
	}

	@Override
	public void removeExisting(int id) {
		Optional<Product> opt = dao.findById(id);
		if(opt.isPresent()) {
			Product p = opt.get();
			if(p.getPrice() * p.getQoh() >= PRODUCT_DELETION_THRESHOLD) {
				throw new IllegalStateException("Delete prevention threshold is "+PRODUCT_DELETION_THRESHOLD+", product value is higher");
			}
			dao.deleteById(id);
		}
	}

	@Override
	public Optional<Product> findById(int id) {
		return dao.findById(id);
	}

	@Override
	public List<Product> findAll() {
		return dao.findAll();
	}

}
