package com.cisco.training.dal;

import java.util.List;
import java.util.Optional;

import javax.persistence.EntityManager;
import javax.persistence.Query;
import javax.persistence.TypedQuery;

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
	
	//container check if caller started tx, else begin
	@Override
	public Product save(Product toBeSaved) {
		//new
		em.persist(toBeSaved);
		//managed
		return toBeSaved;
	}
	//if started for this method, then end tx -> detached

	@Override
	public Optional<Product> findById(int id) {
		Product p = em.find(Product.class, id);
		//p ---> managed
		return p == null ? Optional.empty() : Optional.of(p);
	}

	@Override
	public List<Product> findAll() {
		//give java object name not table name
		TypedQuery<Product> q = em.createQuery("seLect p from Product as p", Product.class);
		return q.getResultList();
	}

	@Override
	public void deleteById(int id) {
		//from javax.persistence class
		Query q = em.createQuery("delete from Product p where p.id=:idParam");
		q.setParameter("idParam", id);
		q.executeUpdate();
		
//		Product p = em.find(Product.class, id);
//		em.remove(p);
		
	}
	

}
