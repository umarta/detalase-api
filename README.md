# Getting started

TODO: Add Description

## How to Build

The generated code has dependencies over external libraries like UniRest. These dependencies are defined in the ```composer.json``` file that comes with the SDK. 
To resolve these dependencies, we use the Composer package manager which requires PHP greater than 5.3.2 installed in your system. 
Visit [https://getcomposer.org/download/](https://getcomposer.org/download/) to download the installer file for Composer and run it in your system. 
Open command prompt and type ```composer --version```. This should display the current version of the Composer installed if the installation was successful.

* Using command line, navigate to the directory containing the generated files (including ```composer.json```) for the SDK. 
* Run the command ```composer install```. This should install all the required dependencies and create the ```vendor``` directory in your project directory.

![Building SDK - Step 1](https://apidocs.io/illustration/php?step=installDependencies&workspaceFolder=detalase-api-PHP)

### [For Windows Users Only] Configuring CURL Certificate Path in php.ini

CURL used to include a list of accepted CAs, but no longer bundles ANY CA certs. So by default it will reject all SSL certificates as unverifiable. You will have to get your CA's cert and point curl at it. The steps are as follows:

1. Download the certificate bundle (.pem file) from [https://curl.haxx.se/docs/caextract.html](https://curl.haxx.se/docs/caextract.html) on to your system.
2. Add curl.cainfo = "PATH_TO/cacert.pem" to your php.ini file located in your php installation. “PATH_TO” must be an absolute path containing the .pem file.

```ini
[curl]
; A default value for the CURLOPT_CAINFO option. This is required to be an
; absolute path.
;curl.cainfo =
```

## How to Use

The following section explains how to use the DetalaseApi library in a new project.

### 1. Open Project in an IDE

Open an IDE for PHP like PhpStorm. The basic workflow presented here is also applicable if you prefer using a different editor or IDE.

![Open project in PHPStorm - Step 1](https://apidocs.io/illustration/php?step=openIDE&workspaceFolder=detalase-api-PHP)

Click on ```Open``` in PhpStorm to browse to your generated SDK directory and then click ```OK```.

![Open project in PHPStorm - Step 2](https://apidocs.io/illustration/php?step=openProject0&workspaceFolder=detalase-api-PHP)     

### 2. Add a new Test Project

Create a new directory by right clicking on the solution name as shown below:

![Add a new project in PHPStorm - Step 1](https://apidocs.io/illustration/php?step=createDirectory&workspaceFolder=detalase-api-PHP)

Name the directory as "test"

![Add a new project in PHPStorm - Step 2](https://apidocs.io/illustration/php?step=nameDirectory&workspaceFolder=detalase-api-PHP)
   
Add a PHP file to this project

![Add a new project in PHPStorm - Step 3](https://apidocs.io/illustration/php?step=createFile&workspaceFolder=detalase-api-PHP)

Name it "testSDK"

![Add a new project in PHPStorm - Step 4](https://apidocs.io/illustration/php?step=nameFile&workspaceFolder=detalase-api-PHP)

Depending on your project setup, you might need to include composer's autoloader in your PHP code to enable auto loading of classes.

```PHP
require_once "../vendor/autoload.php";
```

It is important that the path inside require_once correctly points to the file ```autoload.php``` inside the vendor directory created during dependency installations.

![Add a new project in PHPStorm - Step 4](https://apidocs.io/illustration/php?step=projectFiles&workspaceFolder=detalase-api-PHP)

After this you can add code to initialize the client library and acquire the instance of a Controller class. Sample code to initialize the client library and using controller methods is given in the subsequent sections.

### 3. Run the Test Project

To run your project you must set the Interpreter for your project. Interpreter is the PHP engine installed on your computer.

Open ```Settings``` from ```File``` menu.

![Run Test Project - Step 1](https://apidocs.io/illustration/php?step=openSettings&workspaceFolder=detalase-api-PHP)

Select ```PHP``` from within ```Languages & Frameworks```

![Run Test Project - Step 2](https://apidocs.io/illustration/php?step=setInterpreter0&workspaceFolder=detalase-api-PHP)

Browse for Interpreters near the ```Interpreter``` option and choose your interpreter.

![Run Test Project - Step 3](https://apidocs.io/illustration/php?step=setInterpreter1&workspaceFolder=detalase-api-PHP)

Once the interpreter is selected, click ```OK```

![Run Test Project - Step 4](https://apidocs.io/illustration/php?step=setInterpreter2&workspaceFolder=detalase-api-PHP)

To run your project, right click on your PHP file inside your Test project and click on ```Run```

![Run Test Project - Step 5](https://apidocs.io/illustration/php?step=runProject&workspaceFolder=detalase-api-PHP)

## How to Test

Unit tests in this SDK can be run using PHPUnit. 

1. First install the dependencies using composer including the `require-dev` dependencies.
2. Run `vendor\bin\phpunit --verbose` from commandline to execute tests. If you have 
   installed PHPUnit globally, run tests using `phpunit --verbose` instead.

You can change the PHPUnit test configuration in the `phpunit.xml` file.

## Initialization

### Authentication
In order to setup authentication and initialization of the API client, you need the following information.

| Parameter | Description |
|-----------|-------------|
| oAuthAccessToken | OAuth 2.0 Access Token |



API client can be initialized as following.

```php
$oAuthAccessToken = 'oAuthAccessToken'; // OAuth 2.0 Access Token

$client = new DetalaseApiLib\DetalaseApiClient($oAuthAccessToken);
```


# Class Reference

## <a name="list_of_controllers"></a>List of Controllers

* [AuthController](#auth_controller)
* [HomeController](#home_controller)
* [MyStoreController](#my_store_controller)
* [AreaController](#area_controller)
* [WishController](#wish_controller)
* [ProductController](#product_controller)
* [CartController](#cart_controller)
* [MyProductController](#my_product_controller)
* [ShipController](#ship_controller)
* [OrderController](#order_controller)

## <a name="auth_controller"></a>![Class: ](https://apidocs.io/img/class.png ".AuthController") AuthController

### Get singleton instance

The singleton instance of the ``` AuthController ``` class can be accessed from the API Client.

```php
$auth = $client->getAuth();
```

### <a name="create_login"></a>![Method: ](https://apidocs.io/img/method.png ".AuthController.createLogin") createLogin

> TODO: Add Description


```php
function createLogin(
        $username,
        $password)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| username |  ``` Required ```  | TODO: Add a parameter description |
| password |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```php
$username = 'ayanorma';
$password = 'nirmayanorma123';

$auth->createLogin($username, $password);

```


### <a name="get_check_pid"></a>![Method: ](https://apidocs.io/img/method.png ".AuthController.getCheckPID") getCheckPID

> TODO: Add Description


```php
function getCheckPID()
```

#### Example Usage

```php

$auth->getCheckPID();

```


### <a name="get_update_pid"></a>![Method: ](https://apidocs.io/img/method.png ".AuthController.getUpdatePID") getUpdatePID

> TODO: Add Description


```php
function getUpdatePID()
```

#### Example Usage

```php

$auth->getUpdatePID();

```


[Back to List of Controllers](#list_of_controllers)

## <a name="home_controller"></a>![Class: ](https://apidocs.io/img/class.png ".HomeController") HomeController

### Get singleton instance

The singleton instance of the ``` HomeController ``` class can be accessed from the API Client.

```php
$home = $client->getHome();
```

### <a name="get_index"></a>![Method: ](https://apidocs.io/img/method.png ".HomeController.getIndex") getIndex

> TODO: Add Description


```php
function getIndex()
```

#### Example Usage

```php

$home->getIndex();

```


### <a name="get_popular"></a>![Method: ](https://apidocs.io/img/method.png ".HomeController.getPopular") getPopular

> TODO: Add Description


```php
function getPopular($type)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| type |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```php
$type = 'product_terbaru';

$home->getPopular($type);

```


### <a name="get_new_arrival"></a>![Method: ](https://apidocs.io/img/method.png ".HomeController.getNewArrival") getNewArrival

> TODO: Add Description


```php
function getNewArrival($type)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| type |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```php
$type = 'product_terbaru';

$home->getNewArrival($type);

```


### <a name="get_main_category"></a>![Method: ](https://apidocs.io/img/method.png ".HomeController.getMainCategory") getMainCategory

> TODO: Add Description


```php
function getMainCategory()
```

#### Example Usage

```php

$home->getMainCategory();

```


### <a name="get_all_category"></a>![Method: ](https://apidocs.io/img/method.png ".HomeController.getAllCategory") getAllCategory

> TODO: Add Description


```php
function getAllCategory()
```

#### Example Usage

```php

$home->getAllCategory();

```


[Back to List of Controllers](#list_of_controllers)

## <a name="my_store_controller"></a>![Class: ](https://apidocs.io/img/class.png ".MyStoreController") MyStoreController

### Get singleton instance

The singleton instance of the ``` MyStoreController ``` class can be accessed from the API Client.

```php
$myStore = $client->getMyStore();
```

### <a name="get_index"></a>![Method: ](https://apidocs.io/img/method.png ".MyStoreController.getIndex") getIndex

> TODO: Add Description


```php
function getIndex()
```

#### Example Usage

```php

$myStore->getIndex();

```


### <a name="add_store"></a>![Method: ](https://apidocs.io/img/method.png ".MyStoreController.addStore") addStore

> TODO: Add Description


```php
function addStore(
        $shopName,
        $shopUrl,
        $shopNameThird)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| shopName |  ``` Required ```  | TODO: Add a parameter description |
| shopUrl |  ``` Required ```  | TODO: Add a parameter description |
| shopNameThird |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```php
$shopName = 'test';
$shopUrl = 'test';
$shopNameThird = 'test';

$myStore->addStore($shopName, $shopUrl, $shopNameThird);

```


### <a name="update_store"></a>![Method: ](https://apidocs.io/img/method.png ".MyStoreController.updateStore") updateStore

> TODO: Add Description


```php
function updateStore(
        $shopName,
        $shopUrl,
        $shopNameThird,
        $storeId)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| shopName |  ``` Required ```  | TODO: Add a parameter description |
| shopUrl |  ``` Required ```  | TODO: Add a parameter description |
| shopNameThird |  ``` Required ```  | TODO: Add a parameter description |
| storeId |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```php
$shopName = 'lagi';
$shopUrl = 's';
$shopNameThird = 'ss';
$storeId = 51;

$myStore->updateStore($shopName, $shopUrl, $shopNameThird, $storeId);

```


### <a name="get_edit_store"></a>![Method: ](https://apidocs.io/img/method.png ".MyStoreController.getEditStore") getEditStore

> TODO: Add Description


```php
function getEditStore()
```

#### Example Usage

```php

$myStore->getEditStore();

```


### <a name="get_market"></a>![Method: ](https://apidocs.io/img/method.png ".MyStoreController.getMarket") getMarket

> TODO: Add Description


```php
function getMarket()
```

#### Example Usage

```php

$myStore->getMarket();

```


[Back to List of Controllers](#list_of_controllers)

## <a name="area_controller"></a>![Class: ](https://apidocs.io/img/class.png ".AreaController") AreaController

### Get singleton instance

The singleton instance of the ``` AreaController ``` class can be accessed from the API Client.

```php
$area = $client->getArea();
```

### <a name="get_province"></a>![Method: ](https://apidocs.io/img/method.png ".AreaController.getProvince") getProvince

> TODO: Add Description


```php
function getProvince()
```

#### Example Usage

```php

$area->getProvince();

```


### <a name="get_city"></a>![Method: ](https://apidocs.io/img/method.png ".AreaController.getCity") getCity

> key|value
> --- | --- 
> province_id|id


```php
function getCity($cityId)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| cityId |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```php
$cityId = 1;

$area->getCity($cityId);

```


### <a name="get_district"></a>![Method: ](https://apidocs.io/img/method.png ".AreaController.getDistrict") getDistrict

> key|value
> ---|---
> province_id|id
> city_id|id


```php
function getDistrict($cityId)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| cityId |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```php
$cityId = 1;

$area->getDistrict($cityId);

```


### <a name="get_sub_district"></a>![Method: ](https://apidocs.io/img/method.png ".AreaController.getSubDistrict") getSubDistrict

> param|value
> ---|---
> province_id|id
> city_id|id
> district_id|id


```php
function getSubDistrict($districtId)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| districtId |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```php
$districtId = 1;

$area->getSubDistrict($districtId);

```


[Back to List of Controllers](#list_of_controllers)

## <a name="wish_controller"></a>![Class: ](https://apidocs.io/img/class.png ".WishController") WishController

### Get singleton instance

The singleton instance of the ``` WishController ``` class can be accessed from the API Client.

```php
$wish = $client->getWish();
```

### <a name="get_my_wish"></a>![Method: ](https://apidocs.io/img/method.png ".WishController.getMyWish") getMyWish

> today


```php
function getMyWish(
        $type,
        $contentType)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| type |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```php
$type = 'myList';
$contentType = 'application/x-www-form-urlencoded';

$wish->getMyWish($type, $contentType);

```


### <a name="create_del_image"></a>![Method: ](https://apidocs.io/img/method.png ".WishController.createDelImage") createDelImage

> TODO: Add Description


```php
function createDelImage(
        $contentType,
        $id,
        $pic)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| contentType |  ``` Required ```  | TODO: Add a parameter description |
| id |  ``` Required ```  | TODO: Add a parameter description |
| pic |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```php
$contentType = 'application/x-www-form-urlencoded';
$id = 71;
$pic = 2;

$wish->createDelImage($contentType, $id, $pic);

```


### <a name="create_reply_handler"></a>![Method: ](https://apidocs.io/img/method.png ".WishController.createReplyHandler") createReplyHandler

> TODO: Add Description


```php
function createReplyHandler(
        $contentType,
        $id)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| contentType |  ``` Required ```  | TODO: Add a parameter description |
| id |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```php
$contentType = 'application/x-www-form-urlencoded';
$id = 71;

$wish->createReplyHandler($contentType, $id);

```


### <a name="add_wish"></a>![Method: ](https://apidocs.io/img/method.png ".WishController.addWish") addWish

> TODO: Add Description


```php
function addWish(
        $contentType,
        $name,
        $pic1,
        $price,
        $link,
        $pic2,
        $pic3)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| contentType |  ``` Required ```  | TODO: Add a parameter description |
| name |  ``` Required ```  | TODO: Add a parameter description |
| pic1 |  ``` Required ```  | TODO: Add a parameter description |
| price |  ``` Required ```  | TODO: Add a parameter description |
| link |  ``` Required ```  | TODO: Add a parameter description |
| pic2 |  ``` Required ```  | TODO: Add a parameter description |
| pic3 |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```php
$contentType = 'application/json';
$name = 'sa';
$pic1 = 'pic1';
$price = 1234;
$link = 'http://aa.aa/cc';
$pic2 = 'pic2';
$pic3 = 'pic3';

$wish->addWish($contentType, $name, $pic1, $price, $link, $pic2, $pic3);

```


### <a name="get_edit_wish"></a>![Method: ](https://apidocs.io/img/method.png ".WishController.getEditWish") getEditWish

> TODO: Add Description


```php
function getEditWish($id)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| id |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```php
$id = 71;

$wish->getEditWish($id);

```


### <a name="update_wish"></a>![Method: ](https://apidocs.io/img/method.png ".WishController.updateWish") updateWish

> TODO: Add Description


```php
function updateWish(
        $name,
        $price,
        $link,
        $pic1,
        $pic2,
        $pic3,
        $id)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| name |  ``` Required ```  | TODO: Add a parameter description |
| price |  ``` Required ```  | TODO: Add a parameter description |
| link |  ``` Required ```  | TODO: Add a parameter description |
| pic1 |  ``` Required ```  | TODO: Add a parameter description |
| pic2 |  ``` Required ```  | TODO: Add a parameter description |
| pic3 |  ``` Required ```  | TODO: Add a parameter description |
| id |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```php
$name = 'sasd';
$price = 1234;
$link = 'http://aa.aa/cc';
$pic1 = 'pic1';
$pic2 = 'pic2';
$pic3 = 'pic3';
$id = 21;

$wish->updateWish($name, $price, $link, $pic1, $pic2, $pic3, $id);

```


### <a name="create_delete_wish"></a>![Method: ](https://apidocs.io/img/method.png ".WishController.createDeleteWish") createDeleteWish

> TODO: Add Description


```php
function createDeleteWish($idList)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| idList |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```php
$idList = 1;

$wish->createDeleteWish($idList);

```


[Back to List of Controllers](#list_of_controllers)

## <a name="product_controller"></a>![Class: ](https://apidocs.io/img/class.png ".ProductController") ProductController

### Get singleton instance

The singleton instance of the ``` ProductController ``` class can be accessed from the API Client.

```php
$product = $client->getProduct();
```

### <a name="get_product"></a>![Method: ](https://apidocs.io/img/method.png ".ProductController.getProduct") getProduct

> param | value 
> 
> --- | --- 
> 
> cat | categories_id1 
> 
> cat2 | categories_id2
> 
> cat3 | categories_id3
> 
> cat4 | categories_id4


```php
function getProduct(
        $type,
        $id,
        $priceRange)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| type |  ``` Required ```  | TODO: Add a parameter description |
| id |  ``` Required ```  | TODO: Add a parameter description |
| priceRange |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```php
$type = 1;
$id = 5;
$priceRange = '0,100000';

$product->getProduct($type, $id, $priceRange);

```


### <a name="search_input"></a>![Method: ](https://apidocs.io/img/method.png ".ProductController.searchInput") searchInput

> search parameter : src
> ex : {{url}}/product/searchInput?src=fashion


```php
function searchInput($src)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| src |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```php
$src = 'fashion';

$product->searchInput($src);

```


### <a name="search_result"></a>![Method: ](https://apidocs.io/img/method.png ".ProductController.searchResult") searchResult

> TODO: Add Description


```php
function searchResult($src)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| src |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```php
$src = 'fashion';

$product->searchResult($src);

```


### <a name="create_save_my_product"></a>![Method: ](https://apidocs.io/img/method.png ".ProductController.createSaveMyProduct") createSaveMyProduct

> TODO: Add Description


```php
function createSaveMyProduct(
        $id,
        $value)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| id |  ``` Required ```  | TODO: Add a parameter description |
| value |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```php
$id = 3;
$value = 'Size (clothing):S_Color (costume):Blue Dark';

$product->createSaveMyProduct($id, $value);

```


### <a name="create_save_bulk_product"></a>![Method: ](https://apidocs.io/img/method.png ".ProductController.createSaveBulkProduct") createSaveBulkProduct

> TODO: Add Description


```php
function createSaveBulkProduct($id)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| id |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```php
$id = 1;

$product->createSaveBulkProduct($id);

```


### <a name="get_prod_detail"></a>![Method: ](https://apidocs.io/img/method.png ".ProductController.getProdDetail") getProdDetail

> param|value
> ---|---
> id|product_id/spu_id


```php
function getProdDetail($id)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| id |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```php
$id = 3;

$product->getProdDetail($id);

```


### <a name="get_cat"></a>![Method: ](https://apidocs.io/img/method.png ".ProductController.getCat") getCat

> TODO: Add Description


```php
function getCat(
        $type,
        $id)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| type |  ``` Required ```  | TODO: Add a parameter description |
| id |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```php
$type = 1;
$id = 1;

$product->getCat($type, $id);

```


### <a name="create_selected_prod"></a>![Method: ](https://apidocs.io/img/method.png ".ProductController.createSelectedProd") createSelectedProd

> TODO: Add Description


```php
function createSelectedProd(
        $id,
        $value)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| id |  ``` Required ```  | TODO: Add a parameter description |
| value |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```php
$id = 473487;
$value = 'Primary color E Type:1_Size (mobile):For Galaxy NOTE 8';

$product->createSelectedProd($id, $value);

```


### <a name="add_to_cart"></a>![Method: ](https://apidocs.io/img/method.png ".ProductController.addToCart") addToCart

> TODO: Add Description


```php
function addToCart(
        $id,
        $value)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| id |  ``` Required ```  | TODO: Add a parameter description |
| value |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```php
$id = 444834;
$value = 'Color (costume):gray';

$product->addToCart($id, $value);

```


[Back to List of Controllers](#list_of_controllers)

## <a name="cart_controller"></a>![Class: ](https://apidocs.io/img/class.png ".CartController") CartController

### Get singleton instance

The singleton instance of the ``` CartController ``` class can be accessed from the API Client.

```php
$cart = $client->getCart();
```

### <a name="add_prod_to_cart"></a>![Method: ](https://apidocs.io/img/method.png ".CartController.addProdToCart") addProdToCart

> TODO: Add Description


```php
function addProdToCart(
        $id,
        $qty)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| id |  ``` Required ```  | TODO: Add a parameter description |
| qty |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```php
$id = 227735;
$qty = 2;

$cart->addProdToCart($id, $qty);

```


### <a name="get_my_cart"></a>![Method: ](https://apidocs.io/img/method.png ".CartController.getMyCart") getMyCart

> TODO: Add Description


```php
function getMyCart($contentType)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| contentType |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```php
$contentType = 'application/json';

$cart->getMyCart($contentType);

```


### <a name="update"></a>![Method: ](https://apidocs.io/img/method.png ".CartController.update") update

> TODO: Add Description


```php
function update(
        $id,
        $qty)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| id |  ``` Required ```  | TODO: Add a parameter description |
| qty |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```php
$id = 'cart:4500822:134:d3b5cbe2-99f5-40f2-8462-b262556359da';
$qty = 10;

$cart->update($id, $qty);

```


### <a name="get_del_cart"></a>![Method: ](https://apidocs.io/img/method.png ".CartController.getDelCart") getDelCart

> TODO: Add Description


```php
function getDelCart($id)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| id |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```php
$id = 'cart:4500822:136:7e054d4e-c2ee-41d5-9f66-7c7e25be63e6';

$cart->getDelCart($id);

```


[Back to List of Controllers](#list_of_controllers)

## <a name="my_product_controller"></a>![Class: ](https://apidocs.io/img/class.png ".MyProductController") MyProductController

### Get singleton instance

The singleton instance of the ``` MyProductController ``` class can be accessed from the API Client.

```php
$myProduct = $client->getMyProduct();
```

### <a name="get_my_product"></a>![Method: ](https://apidocs.io/img/method.png ".MyProductController.getMyProduct") getMyProduct

> add param id for see detail spu


```php
function getMyProduct($id)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| id |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```php
$id = 175730;

$myProduct->getMyProduct($id);

```


### <a name="update_product"></a>![Method: ](https://apidocs.io/img/method.png ".MyProductController.updateProduct") updateProduct

> TODO: Add Description


```php
function updateProduct(
        $title,
        $price,
        $description,
        $etalaseName,
        $id)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| title |  ``` Required ```  | TODO: Add a parameter description |
| price |  ``` Required ```  | TODO: Add a parameter description |
| description |  ``` Required ```  | TODO: Add a parameter description |
| etalaseName |  ``` Required ```  | TODO: Add a parameter description |
| id |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```php
$title = 'test';
$price = 100000;
$description = 'daasa';
$etalaseName = 'etalase_name';
$id = 'id';

$myProduct->updateProduct($title, $price, $description, $etalaseName, $id);

```


### <a name="get_edit_product"></a>![Method: ](https://apidocs.io/img/method.png ".MyProductController.getEditProduct") getEditProduct

> TODO: Add Description


```php
function getEditProduct($id)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| id |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```php
$id = 250108;

$myProduct->getEditProduct($id);

```


### <a name="create_del_product"></a>![Method: ](https://apidocs.io/img/method.png ".MyProductController.createDelProduct") createDelProduct

> TODO: Add Description


```php
function createDelProduct($id)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| id |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```php
$id = 123;

$myProduct->createDelProduct($id);

```


### <a name="create_delete_spu"></a>![Method: ](https://apidocs.io/img/method.png ".MyProductController.createDeleteSPU") createDeleteSPU

> TODO: Add Description


```php
function createDeleteSPU($id)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| id |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```php
$id = 126;

$myProduct->createDeleteSPU($id);

```


### <a name="get_download"></a>![Method: ](https://apidocs.io/img/method.png ".MyProductController.getDownload") getDownload

> TODO: Add Description


```php
function getDownload(
        $id,
        $contentType)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| id |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```php
$id =  175730;
$contentType = 'application/json';

$myProduct->getDownload($id, $contentType);

```


[Back to List of Controllers](#list_of_controllers)

## <a name="ship_controller"></a>![Class: ](https://apidocs.io/img/class.png ".ShipController") ShipController

### Get singleton instance

The singleton instance of the ``` ShipController ``` class can be accessed from the API Client.

```php
$ship = $client->getShip();
```

### <a name="create_count_ship_fee"></a>![Method: ](https://apidocs.io/img/method.png ".ShipController.createCountShipFee") createCountShipFee

> TODO: Add Description


```php
function createCountShipFee(
        $provinceId,
        $cityId,
        $districtId,
        $subDistrictId,
        $kg)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| provinceId |  ``` Required ```  | TODO: Add a parameter description |
| cityId |  ``` Required ```  | TODO: Add a parameter description |
| districtId |  ``` Required ```  | TODO: Add a parameter description |
| subDistrictId |  ``` Required ```  | TODO: Add a parameter description |
| kg |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```php
$provinceId = 1;
$cityId = 1;
$districtId = 1;
$subDistrictId = 1;
$kg = 1;

$ship->createCountShipFee($provinceId, $cityId, $districtId, $subDistrictId, $kg);

```


[Back to List of Controllers](#list_of_controllers)

## <a name="order_controller"></a>![Class: ](https://apidocs.io/img/class.png ".OrderController") OrderController

### Get singleton instance

The singleton instance of the ``` OrderController ``` class can be accessed from the API Client.

```php
$order = $client->getOrder();
```

### <a name="create_checkout"></a>![Method: ](https://apidocs.io/img/method.png ".OrderController.createCheckout") createCheckout

> TODO: Add Description


```php
function createCheckout(
        $contentType,
        $body)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| contentType |  ``` Required ```  | TODO: Add a parameter description |
| body |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```php
$contentType = 'application/json';
$bodyValue = "{\r\n  \"product\": [\r\n    {\r\n      \"id\": \"cart:7638:210359:a5fc59b9-0761-45c8-8506-bdbb1261c81e\"\r\n    },\r\n    {\r\n      \"id\": \"cart:4500822:134:4dd8f65e-e446-4f67-98e6-ca5efb0e5d93\"\r\n    },\r\n    {\r\n      \"id\": \"cart:7638:228827:c20e6ec3-f0e8-4792-a73d-f51dd8552470\"\r\n    }\r\n  ],\r\n  \"person\": {\r\n    \"address_id\": 1,\r\n    \"address\": \"assasa\",\r\n    \"phone\": \"09921\",\r\n    \"name\": \"obi bangsat\"\r\n  }\r\n}";
$body = APIHelper::deserialize($bodyValue);

$order->createCheckout($contentType, $body);

```


### <a name="change_cost"></a>![Method: ](https://apidocs.io/img/method.png ".OrderController.changeCost") changeCost

> TODO: Add Description


```php
function changeCost(
        $contentType,
        $body)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| contentType |  ``` Required ```  | TODO: Add a parameter description |
| body |  ``` Required ```  ``` Collection ```  | TODO: Add a parameter description |



#### Example Usage

```php
$contentType = 'application/json';
$bodyValue = "[\r\n  {\r\n    \"id\": \"cart:4500822:134:4dd8f65e-e446-4f67-98e6-ca5efb0e5d93\"\r\n  },\r\n  {\r\n    \"id\": \"cart:4500822:134:4dd8f65e-e446-4f67-98e6-ca5efb0e5d93\"\r\n  }\r\n]";
$body = APIHelper::deserialize($bodyValue);

$order->changeCost($contentType, $body);

```


### <a name="create_cost_ship"></a>![Method: ](https://apidocs.io/img/method.png ".OrderController.createCostShip") createCostShip

> TODO: Add Description


```php
function createCostShip(
        $contentType,
        $body)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| contentType |  ``` Required ```  | TODO: Add a parameter description |
| body |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```php
$contentType = 'application/json';
$bodyValue = "{\r\n  \"person\": {\r\n    \"province_id\": \"10\",\r\n    \"province_name\": \"DKI Jakarta\",\r\n    \"city_id\": \"2494\",\r\n    \"city_name\": \"Kota Jakarta Utara\",\r\n    \"sub_district_id\": \"1395\",\r\n    \"sub_district_name\": \"Tanjung Priok\",\r\n    \"district_id\": \"18156\",\r\n    \"district_name\": \"Sungai Bambu\",\r\n    \"address_id\": \"18156\",\r\n    \"name\": \"ds\",\r\n    \"address\": \"ds\",\r\n    \"phone\": \"12321\"\r\n  },\r\n  \"product\": [\r\n    {\r\n      \"id\": \"cart:7638:228579:2848cc97-f933-4d0e-973d-cf44b16aea4d\"\r\n    }\r\n  ]\r\n}";
$body = APIHelper::deserialize($bodyValue);

$order->createCostShip($contentType, $body);

```


### <a name="get_my_order"></a>![Method: ](https://apidocs.io/img/method.png ".OrderController.getMyOrder") getMyOrder

> TODO: Add Description


```php
function getMyOrder($type)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| type |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```php
$type = 1;

$order->getMyOrder($type);

```


### <a name="get_pkg_status"></a>![Method: ](https://apidocs.io/img/method.png ".OrderController.getPkgStatus") getPkgStatus

> TODO: Add Description


```php
function getPkgStatus()
```

#### Example Usage

```php

$order->getPkgStatus();

```


### <a name="get_order_trace_seq"></a>![Method: ](https://apidocs.io/img/method.png ".OrderController.getOrderTraceSeq") getOrderTraceSeq

> TODO: Add Description


```php
function getOrderTraceSeq($type)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| type |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```php
$type = 1;

$order->getOrderTraceSeq($type);

```


### <a name="get_order_status"></a>![Method: ](https://apidocs.io/img/method.png ".OrderController.getOrderStatus") getOrderStatus

> TODO: Add Description


```php
function getOrderStatus(
        $id,
        $item)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| id |  ``` Required ```  | TODO: Add a parameter description |
| item |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```php
$id = 2019062700000011;
$item = 10356;

$order->getOrderStatus($id, $item);

```


### <a name="get_re_pay"></a>![Method: ](https://apidocs.io/img/method.png ".OrderController.getRePay") getRePay

> TODO: Add Description


```php
function getRePay($id)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| id |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```php
$id = 2019072400000002;

$order->getRePay($id);

```


### <a name="get_on_proccess"></a>![Method: ](https://apidocs.io/img/method.png ".OrderController.getOnProccess") getOnProccess

> TODO: Add Description


```php
function getOnProccess()
```

#### Example Usage

```php

$order->getOnProccess();

```


[Back to List of Controllers](#list_of_controllers)



