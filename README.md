AT Command Command Description Return Value

AT+CMQTTSTART -> Enable MQTT service -> OK

AT+CMQTTACCQ=0,"Waveshare-Sim7028",0 -> Apply for MQTT client -> OK

AT+CMQTTCONNECT=0,"tcp://mqtt.easyiothings.com",20,1 -> Send MQTT request, connect the private MQTT server (MQTTS) -> OK

AT+CMQTTTOPIC=0,11 -> Input the message topic to be published  -> >sim7028test OK

AT+CMQTTPAYLOAD=0,9  ->  Input the published message  -> OK >waveshare

AT+CMQTTPUB=0,0,60 -> Publish the message -> OK +CMQTTPUB: 0,0

AT+CMQTTSUB=0,4,1 -> Subscribe to the message topics -> >test OK +CMQTTSUBTOPIC: 0,0

[10:03:39.665]receive ←◆ +CMQTTRXSTART: 0,4,18 +CMQTTRXTOPIC: 0,4 test +CMQTTRXPAYLOAD: 0,18 { "msg": "hello" } +CMQTTRXEND: 0

AT+CMQTTSTOP -> Stop MQTT service -> OK

AT+CMQTTREL -> Release client terminal -> OK

AT+CMQTTUNSUBTOPIC -> Release the subscribed topics -> OK

AT+CMQTTUNSUB -> Release Subscription -> OK