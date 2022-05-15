package com.cisco.training.service;

import org.springframework.context.annotation.Profile;
import org.springframework.stereotype.Service;

@Profile("smsdisabled")
@Service
public class IgnoringSMSGateway implements SMSGateway{

	@Override
	public void sendSMS(String phNo, String msg) {
		System.out.println("--------- Ignoring SMS to "+phNo+"---------");
		
	}

}
