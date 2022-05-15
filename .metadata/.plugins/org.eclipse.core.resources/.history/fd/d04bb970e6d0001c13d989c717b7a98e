package com.cisco.training.service;

import org.springframework.context.annotation.Profile;
import org.springframework.stereotype.Service;

@Profile("smsenabled")
@Service
public class RealSMSGateway implements SMSGateway{

	@Override
	public void sendSMS(String phNo, String msg) {
		System.out.println("[[[[[[[[[[[ Sending SMS to "+phNo+"]]]]]]]]]]]");
		//imagine it to send real sms to your phone
	}

}