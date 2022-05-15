package com.cisco.training.dal;

import java.util.ArrayList;
import java.util.HashMap;
import java.util.List;
import java.util.Map;
import java.util.Optional;

import com.cisco.training.domain.Product;

public class ProductDAOInMemImpl implements ProductDAO{
	
	Map<Integer, Product> db = new HashMap<>();
	int idSequence = 0;

	@Override
	public Product save(Product toBeSaved) {
		int id = ++idSequence;
		toBeSaved.setId(id);
		db.put(id, toBeSaved);
		return toBeSaved;
	}

	@Override
	public Optional<Product> findById(int id) {
		Product p = db.get(id);
		if(p == null) {
			return Optional.empty();
		}else {
			return Optional.of(p);
		}
	}

	@Override
	public List<Product> findAll() {
		return new ArrayList<>(db.values());
	}

	@Override
	public void deleteById(int id) {
		db.remove(id);		
	}

}
