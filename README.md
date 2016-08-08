Yii libphonenumber

Installation 

Download and extract extension files to the directory protected/vendors

Usage 

Wherever you want to validate the phone number,use the following codes

Yii::setPathOfAlias('libphonenumber',Yii::getPathOfAlias('application.vendors.libphonenumber'));
 
$phonenumber=new libphonenumber\LibPhone($your_phone_number);
 
/**
  * Checking the number is valid or not  
  *
  * @return boolean
  */
$phonenumber->validate();   //return true if valid
 
//to convert to international format
$phonenumber->toInternational();
 
//to get national format
$phonenumber->toNational();
 
//to get E164 format
$phonenumber->toE164();
 
/*to get out of country calling number format
 *need to pass the region value
 */
$phonenumber->toOutOfCountryCallingNumber($region);

