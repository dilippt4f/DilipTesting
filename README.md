# Order Service #

[http://denish_t4f_order_services](http://denish_t4f_order_services "Order Service")

## Get Orders

> `GET /order`

#### request
 
parameter 			| type		| description		| default	| required
 ----------			|---------- |----------			| --------	| --------
per_page			| int		| per page records 	| 20		| no
page				| int		| page no. 1,2,3 etc| 1			| no
old_product_id		| int		| old product Id	| N/A		| no
sort_type			| string	| asc,desc			| asc		| no
sort_by				| string	| sort by field		| N/A		| no
status_id			| int		| order status id	| N/A		| no
customer_name		| string	| customer name		| N/A		| no
subscriber_email	| string	| customer email	| N/A		| no
subscriber_telephone| string	| customer email	| N/A		| no
depature_date_max	| date		| departure date max| N/A		| no
depature_date_min	| date		| departure date min| N/A		| no
search_id			| string/int		| providerId, productId, orderId, provider name, provider tour code,  product name or product code 				| N/A 		| no
provider_id			| int		| provider id		| N/A		| no
invoice_no			| string	| invoice number	| N/A		| no
invoice_amount		| string	| invoice amount	| N/A		| no
order_created_min	| date		| order created date min |	N/A	| no
order_created_max	| date		| order created date max |	N/A	| no
platform			| int	 	| 0,1,2,5,6,7( 0 = Web Site,											1 = Telephone,2 = APP (T4F),5 = M Site (TFF),6 = OPEN API,7 = APP		| N/A		| no


#### result

 parameter 	| type		| description
 ----------	|---------- |----------	
 status		| int 		| 200=success , 0=error
 message  	| string 	| message of return
 data 		| json array| return each order detail 

e.g.

	For No Record Found:
	{
	    "code": 0,
	    "status": 200,
	    "message": "success",
	    "data": null
	}
	For Success:

    {
    "code": 0,
    "status": 200,
    "message": "success",
    "data": {
	        "total": 232,
	        "per_page": "2",
	        "current_page": 2,
	        "last_page": 116,
	        "next_page_url": "http://denish_t4f_order_services/order?page=3",
	        "prev_page_url": "http://denish_t4f_order_services/order?page=1",
	        "from": 3,
	        "to": 4,
	        "data": [
	            {
	                "order_id": 230,
	                "customer_id": 3416220,
	                "status": 1,
	                "followup_team_type": 0,
	                "platform": 0,
	                "blinking": 0,
	                "purchased_without_account": 1,
	                "payment_info": "",
	                "referer": "",
	                "referer_url": "",
	                "created": "2018-01-24 21:24:53",
	                "last_updated": "2 days",
	                "lastUpdatedBy": 117,
	                "customer": {
	                    "order_id": 230,
	                    "customer_name": "",
	                    "customer_email": "denishk.bilp@gmail.com"
	                },
	                "order_total": [
	                    {
	                        "order_total_id": 452,
	                        "class": "ot_subtotal",
	                        "value": "290.40",
	                        "title": "Subtotal: ",
	                        "text": "$290.40",
	                        "sort_order": 760,
	                        "order_id": 230,
	                        "order_product_id": 1
	                    },
	                    {
	                        "order_total_id": 453,
	                        "class": "ot_total",
	                        "value": "290.40",
	                        "title": "Total: ",
	                        "text": "<b>$290.40</b>",
	                        "sort_order": 800,
	                        "order_id": 230,
	                        "order_product_id": 1
	                    }
	                ],
	                "order_product": [
	                    {
	                        "order_id": 230,
	                        "order_product_id": 260,
	                        "order_product_tour": {
	                            "order_product_id": 260,
	                            "provider_id": 81,
	                            "product_id": 101457840,
	                            "provider_tour_code": "NYLL-DN3tt",
	                            "departure_date": "2018-02-27 00:00:00",
	                            "departure_time": "07:00:00"
	                        }
	                    }
	                ]
	            },
	            {
	                "order_id": 229,
	                "customer_id": 3416220,
	                "status": 1,
	                "followup_team_type": 0,
	                "platform": 0,
	                "blinking": 0,
	                "purchased_without_account": 1,
	                "payment_info": "",
	                "referer": "",
	                "referer_url": "",
	                "created": "2018-01-24 21:16:46",
	                "last_updated": "1 day",
	                "lastUpdatedBy": 117,
	                "customer": {
	                    "order_id": 229,
	                    "customer_name": "",
	                    "customer_email": "denishk.bilp@gmail.com"
	                },
	                "order_total": [
	                    {
	                        "order_total_id": 450,
	                        "class": "ot_subtotal",
	                        "value": "290.40",
	                        "title": "Subtotal: ",
	                        "text": "$290.40",
	                        "sort_order": 760,
	                        "order_id": 229,
	                        "order_product_id": 1
	                    },
	                    {
	                        "order_total_id": 451,
	                        "class": "ot_total",
	                        "value": "290.40",
	                        "title": "Total: ",
	                        "text": "<b>$290.40</b>",
	                        "sort_order": 800,
	                        "order_id": 229,
	                        "order_product_id": 1
	                    }
	                ],
	                "order_product": [
	                    {
	                        "order_id": 229,
	                        "order_product_id": 259,
	                        "order_product_tour": {
	                            "order_product_id": 259,
	                            "provider_id": 81,
	                            "product_id": 101457840,
	                            "provider_tour_code": "NYLL-DN3tt",
	                            "departure_date": "2018-02-28 00:00:00",
	                            "departure_time": "07:00:00"
	                        }
	                    }
	                ]
	            }
	        ]
	    }
	}



---

## Get Tour URL 

> `GET /{productID}/url`

#### request
 
parameter 	| type		| description	| default	| required
 ----------	|---------- |----------		| --------	| --------
languageId	| int		| 1,2,3 		| 1			| no



#### result

parameter 	| type			| description	
 ----------	|---------- 	|----------		
status		| int 			| 200=success , 0=error 
message  	| string 		| message of return 
data 		| json string 	| return tour url

e.g.

	For Error:
	{
    	"status": 0,
	    "message": "No product URL found!"
	}
    
	For Success:

    {
	    "status": 200,
	    "message": "success",
	    "data": "sic-tour-mangrove-swamp-cruise-from-kuching-spanish"
	}

---



## Get display price for product 

> `GET /{productID}/price/display`

#### request

parameter 		| type		| description	| default		| required
 ----------		|---------- |----------		| --------		| --------  
currency		| string 	| USD,EUR,INR	| USD			| No
isAffiliate		| boolean	| true,false	| false			| No
format			| string 	| number_format	| number_format	| No
platform		| string 	| pc,mobile		| pc			| No


#### result

parameter 		| type		| description	
----------		|---------- |----------	
status			| int 		| 200=success , 0=error
message  		| string 	| message of return
data 			| json array| return def. price,value,special price,currency, on_sale

e.g.

	For Error:
	{
    	"status": 0,
	    "message": "Product price not found!"
	}
    
	For Success:

    {
	    "status": 200,
	    "message": "success",
	    "data": {
	        "default_price": 240,
	        "target_default_price": "$240.00",
	        "target_default_price_value": "240.00",
	        "on_sale": false,
	        "special_price": false,
	        "target_special_price": 0,
	        "target_special_price_value": 0,
	        "default_save_price": 0,
	        "target_save_price": 0,
	        "currency_code": "USD",
	        "target_currency": "USD"
	    }
	}

---

## Get T4F Extra Values for Tour 

> `post /get-product-extra-values`

#### request

parameter 		| type		| description			| default		| required
 ----------		|---------- |----------				| --------		| --------
id				| array 	| [101457588,101818281] | N/A			| Yes	

#### result

parameter 		| type		| description	
 ----------		|---------- |----------
status			| int 		| 200=success , 0=error
message  		| string 	| message of return
data 			| json array| return product extra values t4f

e.g.

	For Error:
	{
	    "status": 0,
	    "message": "something went wrong!"
	}
    
	For Success:

    {
	    "status": 200,
	    "message": "success",
	    "data": {
	        "101457588": {
	            "region_id": 1,
	            "vacation_package": 1,
	            "advertised_price_t4f": "598.0000",
	            "display_room_option": 1,
	            "display_calendar": 1,
	            "api_source": "",
	            "max_num_guest": 4,
	            "small_group_size": 0,
	            "rankwise_sort": 0,
	            "passenger_info": "{\"en\":{\"is_required_only_lead_traveler\":0,\"first_name\":{\"label\":\"First Name\",\"title\":\"First Name\",\"name\":\"first_name\",\"type\":\"text\",\"options\":[],\"min\":\"\",\"max\":\"\"},\"last_name\":{\"label\":\"Last Name\",\"title\":\"Last Name\",\"name\":\"last_name\",\"type\":\"text\",\"options\":[],\"min\":\"\",\"max\":\"\"},\"extra_field_2\":{\"label\":\"Is child birthday required?\",\"title\":\"Child Birth Date\",\"name\":\"child_birth_date\",\"type\":\"date\",\"options\":[],\"min\":\"\",\"max\":\"\"}},\"es\":{\"is_required_only_lead_traveler\":0,\"first_name\":{\"label\":\"First Name\",\"title\":\"First Name\",\"name\":\"first_name\",\"type\":\"text\",\"options\":[],\"min\":\"\",\"max\":\"\"},\"last_name\":{\"label\":\"Last Name\",\"title\":\"Last Name\",\"name\":\"last_name\",\"type\":\"text\",\"options\":[],\"min\":\"\",\"max\":\"\"}}}",
	            "product_type_id": 1
	        },
	        "101818281": {
	            "region_id": 1,
	            "vacation_package": 0,
	            "advertised_price_t4f": "54.0000",
	            "display_room_option": 0,
	            "display_calendar": 1,
	            "api_source": "Rezdy",
	            "max_num_guest": 0,
	            "small_group_size": 0,
	            "rankwise_sort": 0,
	            "passenger_info": "{\"en\":{\"is_required_only_lead_traveler\":0,\"first_name\":{\"label\":\"First Name\",\"title\":\"First Name\",\"name\":\"first_name\",\"type\":\"text\",\"options\":[],\"min\":\"\",\"max\":\"\"},\"last_name\":{\"label\":\"Last Name\",\"title\":\"Last Name\",\"name\":\"last_name\",\"type\":\"text\",\"options\":[],\"min\":\"\",\"max\":\"\"},\"extra_field_1\":{\"label\":\"Is adult birthday required?\",\"title\":\"Adult Birth Date\",\"name\":\"date_of_birth\",\"type\":\"date\",\"options\":[],\"min\":\"\",\"max\":\"\"},\"extra_field_2\":{\"label\":\"Is child birthday required?\",\"title\":\"Child Birth Date\",\"name\":\"child_birth_date\",\"type\":\"date\",\"options\":[],\"min\":\"\",\"max\":\"\"},\"extra_field_3\":{\"label\":\"Is adult gender required?\",\"title\":\"gender\",\"name\":\"gender\",\"type\":\"radio\",\"options\":[\"Male\",\"Female\"],\"min\":\"\",\"max\":\"\"},\"extra_field_4\":{\"label\":\"Is child gender required?\",\"title\":\"gender\",\"name\":\"gender\",\"type\":\"radio\",\"options\":[\"Male\",\"Female\"],\"min\":\"\",\"max\":\"\"},\"extra_field_7\":{\"label\":\"Is nationality required?\",\"title\":\"nationality\",\"name\":\"guest_nationality\",\"type\":\"text\",\"options\":[],\"min\":\"\",\"max\":\"\"},\"extra_field_8\":{\"label\":\"Is passport no required?\",\"title\":\"passport\",\"name\":\"guest_passport\",\"type\":\"text\",\"options\":[],\"min\":\"\",\"max\":\"\"}},\"es\":{\"is_required_only_lead_traveler\":0,\"first_name\":{\"label\":\"First Name\",\"title\":\"First Name\",\"name\":\"first_name\",\"type\":\"text\",\"options\":[],\"min\":\"\",\"max\":\"\"},\"last_name\":{\"label\":\"Last Name\",\"title\":\"Last Name\",\"name\":\"last_name\",\"type\":\"text\",\"options\":[],\"min\":\"\",\"max\":\"\"}}}",
	            "product_type_id": 10001
	        }
	    }
	}


-----


## Get Tour Note 

> `post /get-tour-note`

#### request

parameter 		| type		| description				| default		| required
 ----------		|---------- |----------					| --------		| --------
productId		| int		| 101818269					| N/A			| No
providerId		| int 		| 5674						| N/A			| No 
duration		| int 		| 6 (No. of days,mins,hrs)	| N/A			| No
durationType    | string	| day,|minute,hour			| day			| No 
langId      	| int		| 1,2						| 1				| No

#### result

parameter 		| type		| description
----------		|---------- |----------			
status			| int 		| 200=success , 0=error
message  		| string 	| message of return
data 			| string 	| product detail tab id:note description

**product detail tab id description**

- 1 : Pricing
- 2 : Package Includes
- 3 : Package Excludes
- 4 : Special Notes
- 5 : Reservation Info
- 6 : Terms and Conditions
- 
e.g.

	For Error:
	{
	    "status": 0,
	    "message": "something went wrong!"
	}
    
	For Success
	{
    "status": 200,
    "message": "success",
    "data": {
        "1": [
            "<br><b><font color=#f7860f>Due to Las Vegas Convention held on Jan 9- Jan 10, 2018, hotel prices may raise. We will do our best to arrange hotels at the lowest prices. However, please be advised that if you stay in Las Vegas hotels during this time period, there may be a surcharge of $100.00-$200.00 per room. The total tour price is subject to final confirmation. Thank you very much for your understanding! </font></b>"
        ],
        "2": [
            "Complimentary pick-up from chosen location (see meeting point) and drop-off"
        ],
        "3": [
            "Airfares or related transportation between your home and New York airport or chosen pick-up location"
        ],
        "4": [
            "<b><font color=#f7860f>Additional expense or Price raise will apply for customers who stay overnight in Las Vegas hotels during Holiday/Event time . The price on our website is not the final price. There may be a price raise. Please be subject to our final confirmation. </font></b>"
        ],
        "5": [
            "1.Immediately after submitting your reservation you will receive a Receipt of Reservation via email.\r\n2. Within one to two business days of submitting your reservation you will receive a confirmation email from us. If you need to book an airline ticket, we recommend that you do so after you receive a confirmation of your tour reservation from us.3. An E-Ticket will be sent to you via email as soon as details of your reservation are confirmed or your supporting information is received by us. We will provide you with all detailed information about your tour on the E-Ticket. Contact information for local tour provider will be included on E-Ticket for your convenience or re-confirmation purpose if re-confirmation is required.4. Simply print your E-Ticket and present it with your valid photo ID on the day of your activity to your tour guide. Please remember E-Ticket is your proof of purchase."
        ],
        "6": [
            "Your purchase does not guarantee confirmation. Your purchase will initiate a reservation process. We will confirm with you via email within one to two business days."
        ]
    }
}


-----


## Get New/Old Product Id, Product Line from URL 

> `get /url_path`

#### request


parameter 		| type		| description										| default		| required
 ----------		|---------- |----------											| --------		| --------
 path			| string	| new-zealand-north-island-self-drive-tour-7-day	| N/A			| Yes
 lang			| string	| en,es												| en			| No 


#### result

parameter 		| type		| description
----------		|---------- |----------											
status			| int 		| 200=success , 0=error
message  		| string 	| message of return
data 			| string 	| product_id, old_product_id, product_line

 
e.g.

	For Error:
	{
	    "status": 0,
	    "message": "Missing url_path!"
	}

	{
	    "status": 0,
	    "message": "No product found for the given url!"
	}
    
	For Success:
	{
	    "status": 200,
	    "message": "success",
	    "data": {
	        "product_id": 101818278,
	        "old_product_id": 467911,
	        "product_line": "tour"
	    }
	}


-----


## Get Multiple Products URLs


> `post /productUrls`

#### request

parameter 			| type		| description			| default		| required
 ----------			|---------- |----------				| --------		| --------
productIds			| array		| [101457618,101457615] | N/A		 	| Yes
lang				| string	| en,es			 	    | en			| No  



#### result

parameter 			| type		| description
----------			|---------- |----------
status				| int 		| 200=success , 0=error
message  			| string 	| message of return
data 				| string 	| productId:URL

 
e.g.

	For Error:
	{
	    "status": 0,
	    "message": "Please provide valid parameters!"
	}

	For Success:
	{
	    "status": 200,
	    "message": "success",
	    "data": {
	        "101457567": "3-day-san-francisco-yosemite-tour",
	        "101457618": "10-day-deluxe-west-coast-tour-package"
	    }
	}


-----


## Get Days Before Tour Can Book (Days Limit)


> `post /get-day-limit`

#### request

parameter 			| type		| description			| default		| required
----------			|---------- |----------				| --------		| --------
productIds[]		| string	| 101457618				| N/A			| Yes
productIds[]		| string	| 101457633				| N/A			| No

*first productIds[] one is required			

#### result

parameter 			| type		| description
----------			|---------- |----------
status				| int 		| 200=success , 0=error
message  			| string 	| message of return
data 				| string 	| productId:days		|


e.g.

	For Error:
	{
	    "status": 0,
	    "message": "Product id not found!"
	}
	
	For Success:
	{
		"status": 200,
		"message": "success",
		"data": {
		    "101457618": 48,
		    "101458038": 0
		}
	}




-----


## Get Tour Type Icon By Product IDs


> `post /get-tour-type-icon`

#### request

parameter 			| type		| description			| default		| required
----------			|---------- |----------				| --------		| --------
| productIds[]		| string	| 101457618				| N/A		 	| Yes
| productIds[]		| string	| 101457633				| N/A		 	| No

*first productIds[] is required

#### result

parameter 			| type		| description
----------			|---------- |----------
status				| int 		| 200=success , 0=error
message  			| string 	| message of return
data 				| string 	| productId:[start_date,end_date,product_id,name,sort_order,product_icon_id]


e.g.

	For Error:
	{
	    "status": 0,
	    "message": "Product id not found!"
	}
	
	For Success:
	{
    "status": 200,
    "message": "success",
    "data": {
        "101818276": [
            {
                "start_date": 0,
                "end_date": 0,
                "product_id": 101818276,
                "product_icon_id": 1,
                "store_id": 2,
                "name": "New Product",
                "sort_order": 15
            },
            {
                "start_date": 0,
                "end_date": 0,
                "product_id": 101818276,
                "product_icon_id": 5,
                "store_id": 2,
                "name": "Buy 2, Get 3rd & 4th Discounted",
                "sort_order": 33
            },
            {
                "start_date": 0,
                "end_date": 0,
                "product_id": 101818276,
                "product_icon_id": 13,
                "store_id": 2,
                "name": "Best Selling",
                "sort_order": 18
            },
            {
                "start_date": 0,
                "end_date": 0,
                "product_id": 101818276,
                "product_icon_id": 14,
                "store_id": 2,
                "name": "Free Airport Pick up",
                "sort_order": 12
            }
        ],
        "101818277": [
            {
                "start_date": 1508140800,
                "end_date": 1514448000,
                "product_id": 101818277,
                "product_icon_id": 3,
                "store_id": 2,
                "name": "Special Offer",
                "sort_order": 24
            },
            {
                "start_date": 0,
                "end_date": 0,
                "product_id": 101818277,
                "product_icon_id": 16,
                "store_id": 2,
                "name": "Free Airport Pick up & Drop off",
                "sort_order": 12
            },
            {
                "start_date": 0,
                "end_date": 0,
                "product_id": 101818277,
                "product_icon_id": 370,
                "store_id": 2,
                "name": "Private Tour ",
                "sort_order": 0
            }
        ]
    }
}


