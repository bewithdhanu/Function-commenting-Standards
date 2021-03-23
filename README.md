# Function-commenting-Standards

Functions:
```
/**
 * Something about the function
 * 
 * Long description for class (if any)...
 *
 * @author    Developer Name <developer@domain.com>
 * @date      @date_with_timezone@
 * @change    Golbal/Region
 * @param     Array/Object/String/Integer/Boolean $varible_name Some description about the parameter
 * @return    Array/Object/String/Integer/Boolean 
 */ 
```
Classes:
```
/**
 * Short description for class
 *
 * Long description for class (if any)...
 *
 * @author          Developer Name <developer@domain.com>
 * @date            @date_with_timezone@
 * @change          Golbal/Region
 * @copyright       @year@ @product_name@
 * @version         Release: @package_version@
 * @link            https://tms.etrucknow.com/@controller_name@
 * @authentication  Required/Not Required
 */ 
 ```
 Code changes inside functions:
 ```
 /**
 * Short description for class
 *
 * Long description for class (if any)...
 *
 * @author          Developer Name <developer@domain.com>
 * @date            @date_with_timezone@
 * @change          Golbal/Region
 * @indicator       Start of change
 */ 
 ...Code here...
 /**
 * @author          Developer Name <developer@domain.com>
 * @indicator       End of change
 */
 ```
 Examples:
 ```
<?php
/**
 * Blog home page
 *
 * Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et 
 * dolore magna aliqua. Ut enim ad minim veniam
 *
 * @author          Dhanu K <dhanu@returntrucks.com>
 * @date            2020-03-34 12:25:11PM IST
 * @change          Golbal
 * @copyright       2021 eTrucknow
 * @version         Release: V1
 * @link            https://tms.etrucknow.com/blog
 * @authentication  Not Required
 */ 
class Blog extends CI_Controller {

        public function __construct()
        {
                parent::__construct();
                // Your own constructor code
        }
        
        /**
         * some description about the first_post function
         * 
         * @author    Dhanu K <dhanu@returntrucks.com>
         * @date      2020-03-34 12:25:11PM IST
         * @change    Golbal
         * @param     String $name User entered name be taken as argment to process something
         * @return    Nothing returning
         */ 
        public function first_post($name)
        {
                // Your own code for the first_post
        }
        
        /**
         * some description about the second_post function
         * 
         * @author    Dhanu K <dhanu@returntrucks.com>
         * @date      2020-03-34 12:25:11PM IST
         * @change    Golbal
         * @param     Integer $id Some bolg item ID passed
         * @param     String $sort Based on sort Asc/Desc user listing will be changed
         * @return    Array returning array of items filtered with sepcif pattern
         */ 
        public function second_post($id,$sort)
        {
                $finalArray = array();
                if ( ! empty( $invoiceParam ) && $invoiceParam != '' ) {
                    $requiredArray = explode( ';', $invoiceParam );
                    if ( ! empty( $requiredArray ) && sizeof( $requiredArray ) > 0 ) {
                        foreach ( $requiredArray as $eachitem ) {
                        
                            /**
                             * some description about code change
                             *
                             * @author          Dhanu K <dhanu@returntrucks.com>
                             * @date            2020-03-34 12:25:11PM IST
                             * @change          Golbal
                             * @indicator       Start of change
                             */ 
                             
                            $explodeArray = explode( '=====', $eachitem );
                            if ( ! empty( $explodeArray ) && sizeof( $explodeArray ) > 0 ) {
                                $key                = $explodeArray[0];
                                $value              = $explodeArray[1];
                                $finalArray[ $key ] = $value;
                            }
                            
                            /**
                             * @author          Dhanu K <dhanu@returntrucks.com>
                             * @indicator       End of change
                             */ 
                             
                        }
                    }
                }
                return $finalArray;
        }
}
 ```
