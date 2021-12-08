# ISO8583-PACK-UNPACK

ISO 8583

Elements </br>
MTI - Message Type Idenitifer (01)
Version  </br>
<ul>
   <li>0XXX Iso 85883 = 1987 Version</li>
        <li>1xxx Iso 8583 = 1993 Version</li>
</ul>
        Message Class
<ul>        
        <li>x1xx Authorization Message</li>
        <li>x2xx Financial Message</li>
        <li>x3xx File Actions Message</li>
        <li>x4xx Reversal & Chargeback Message</li>
        <li>x5xx Reconciliation Message</li>
        <li>x6xx Administrative Message</li>
        <li>x7xx Fee Collection Message</li>
        <li>x8xx Network Management Message</li>
        <li>x9xx Reserved for ISO use</li>
</ul>
	Message Sub Class	
			<li>xx00 For a request, requiring approval</li>
			<li>xx10 For a response to a request</li>
			<li>xx20 For an advice of an action that has already been taken, not requiring approval but still requiring a response</li>
			<li>xx30 For a response to an advice</li>
			<li>xx40 For notification</li>
			<li>xx50 – xx90</li>



Reserved for ISO use BITMAP- DataElements-

Sample</br>
ISO </br>
 02003220000000808000000010000000001500120604120000000112340001840  </br>
 Where 0200 :- Represents Financial request requiring approval of iso8583 version 1987

Json

{
"MTI":"0200",
"PrimaryBitMap":"3220000000808000",
"SecondaryBitMap":"",
"field":{
"3":"000010",
"4":"000000001500",
"7":"1206041200",
"11":"000001",
"41":"12340001",
"49":"840"
}
}
