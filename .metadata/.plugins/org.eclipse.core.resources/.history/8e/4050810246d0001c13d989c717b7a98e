package com.cisco.training.dal;

import java.util.List;
import java.util.Optional;

import javax.persistence.EntityManager;

import org.springframework.beans.factory.annotation.Autowired;
import org.springframework.context.annotation.Primary;
import org.springframework.stereotype.Repository;
import org.springframework.transaction.annotation.Transactional;

import com.cisco.training.domain.Product;

@Primary
@Transactional
@Repository
public class ProductDAOJpaImpl implements ProductDAO{
	
	@Autowired
	EntityManager em;

	@Override
	public Product save(Product toBeSaved) {
		em.persist(toBeSaved);
		return toBeSaved;
	}

	@Override
	public Optional<Product> findById(int id) {
		Product p = em.find(Product.class, id);
		return p == null ? Optional.empty() : Optional.of(p);
	}

	@Override
	public List<Product> findAll() {
		// TODO Auto-generated method stub
		return null;
	}

	@Override
	public void deleteById(int id) {
		Product p = em.find(Product.class, id);
		em.remove(p);		
	}

}
