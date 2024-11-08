# Prisma-Pitplay-Api's

## Owner

### Grounds 

### 1. addGround
- **Old Route**: `/api/app/ground/addGround`
- **New Route**: `/ground/create` 
 
  **Description**: This API endpoint is used to create a new ground.

### 2. getGroundList
- **Old Route**: `/api/app/ground/deleteGround`
- **New Route**: `/ground/all`

  **Description**: Get all grounds.

  **Query Parameters**:
  - `search` (string) – search ground with ground name

### 3. showGround
- **Old Route**: `/api/app/ground/showGround`
- **New Route**: `/ground/showground`
  **Description**: Retrieves information of a specific ground based on its ID.

  **Query Parameters**:
  - `ground_id` – The ID of the ground to be retrieved.

### 4. groundListwithoutFilter
- **Old Route**: `/api/app/ground/groundListwithoutFilter`
- **New Route**: `/ground/withoutfilter`

### 5. deleteGround
- **Old Route**: `/api/app/ground/deleteGround`
- **New Route**: `/ground/delete`
  **Description**: Delete specific ground based on its ID.

  **Query Parameters**:
  - `ground_id` – The ID of the ground to be retrieved.

### 6. updateGround
- **Old Route**: `/api/app/ground/updateGround`
- **New Route**: `/ground/update`

  **Description**: This endpoint updates details of an existing ground.

### 7. ownerGroundSlots
- **Old Route**: `/api/app/ground/owner/timeslots`
- **New Route**: `/ground/owner/timeslots`
  **Description**: Get ground time slots for perticular date and ground.

  **Query Parameters**:
  - `ground_id` – The ID of the ground 
  - `date` (string) – date formate is dd-mm-yyy

### 8. getCountry
- **Old Route**: `/api/app/country`
- **New Route**: `/location/country`

### 9. geState
- **Old Route**: `/api/app/state`
- **New Route**: `/location/state`
  **Query Parameters**:
  - `counrty_id` – The ID of the country 

### 10. getCity
- **Old Route**: `/api/app/city`
- **New Route**: `/location/city`
  **Query Parameters**:
  - `state_id` – The ID of the country 


## Sports 

### 1. addSports
- **Old Route**: `/api/app/ground/addSports`
- **Request method** : `post`
- **New Route**: `/sports`

### 2. allSportsList
- **Old Route**: `/api/app/ground/sportsList`
- **Request method** : `get`
- **New Route**: `/sports`
    **Query Parameters**:
    - `page`
    - `search` - search with sports_name
    - `status` - it is use for get sports status wise on add ground/update ground.

## Service

### 1. addServices
- **Old Route**: `/api/app/ground/addService`
- **Request method** : `post`
- **New Route**: `/service`

### 2. allServiceList
- **Old Route**: `/api/app/ground/serviceList`
- **Request method** : `get`
- **New Route**: `/sports`

    **Query Parameters**:
  - `page`
  - `search` - search with service_name

## User / Auth

### 1. sendOtp
- **Old Route**: `/api/app/auth/sendOtp`
- **New Route**: `/user/sendotp`
- **Pass role = 3 in body for user**
- **Pass role = 2 in body for owner**

### 2. verifyOtp
- **Old Route**: `/api/app/auth/verifyOtp`
- **New Route**: `/user/verifyotp`

### 3. ownerProfile
- **Old Route**: `/api/app/user/getProfile`
- **New Route**: `/user/ownerprofile`

### 4. userList
- **Old Route**: `/api/app/user/userList`
- **New Route**: `/user/list`
  **Query Parameters**:
  - `page`
  - `search` - search with user lists

### 5. updateProfile
- **Old Route**: `/api/app/user/updateProfile`
- **New Route**: `/user/update` 

## Booking

### 1. getAllBookingList
- **Old Route**: `/api/app/booking/allBookings`
- **New Route**: `/booking/owner/allBookings`

  **Query Parameters**:
  - `page`
  - `status` - booked/pending/cancelled
  - `search` - search with ground name, user name

### 2. showbooking
- **Old Route**: `/api/app/booking/showBooking`
- **New Route**: `/booking/owner/showbooking`

    **Query Parameters**:
  - `order_slot_id`

## Coupon 

### 1. addCoupon
- **Old Route**: `/api/app/ground/addCoupon`
- **Request method** : `post`
- **New Route**: `/coupon`

### 2. deleteCoupon
- **Old Route**: `/api/app/ground/deleteCoupon`
- **Request method** : `delete`
- **New Route**: `/coupon`

### 3. getAllCouponList
- **Old Route**: `/api/app/ground/couponList`
- **Request method** : `get`
- **New Route**: `/coupon`

## Dashboard

### 1. ownerDashboard
- **Old Route**: `/api/app/owner/dashboard`
- **New Route**: `/dashboard/owner`


## User

### Ground

### 1. groundTimeSlots
- **Old Route**: `/api/app/ground/groundTimeSlots`
- **New Route**: `/ground/groundtimeslots`
  **Description**: Get ground time slots for perticular date and ground.

  **Query Parameters**:
  - `ground_id` – The ID of the ground 
  - `date` (string) – date formate is dd-mm-yyy

### 2. addGroundReview
- **Old Route**: `/api/app/ground/groundRating`
- **New Route**: `/ground/rating`

### 3. loadmoreReviews
- **Old Route**: `/api/app/ground/loadmoreReviews`
- **New Route**: `/ground/loadmoreReviews`

### 4. searchGround
- **Old Route**: `/api/app/ground/searchGround`
- **New Route**: `/ground/searchground`

### 5. getGroundList
- **Old Route**: `/api/app/user/groundList`
- **New Route**: `/ground/groundlist`
  **Description**: Get nearest ground list.
  **Query Parameters**:
  - `latitude`(string) 
  - `longitude`(string) 
  - `sortby` (string) – far or near
  - `page` 
  - `sports`(string) – sports_name
  - `distance_type`(string) – e.g 10 in km

### User

### 1. getAuthorization(Guest User)
- **Old Route**: `/api/app/auth/getAuthorization`
- **New Route**: `/user/getauthorization`

### 2. userProfile
- **Old Route**: `/api/app/auth/getprofiledata`
- **New Route**: `/user/profile`

### 3. coverImageUpload
- **Old Route**: `/api/app/auth/updateCoverPhoto/:id`
- **Note**: In this new route no need to pass :id in params. we take it from header key.
- **New Route**: `/user/coverimageupload`

### 4. uploadProfilePhoto
- **Old Route**: `/api/app/auth/updatephoto/:id`
- **Note**: In this new route no need to pass :id in params. we take it from header key.
- **New Route**: `user/profileimageupload`

### 5. deleteProfile
- **Old Route**: `/api/app/user/deleteProfile/:id`
- **Note**: In this new route no need to pass :id in params. we take it from header key.
- **New Route**: `/user/delete`

## Booking

### 1. createBooking
- **Old Route**: `/api/app/booking/createBooking`
- **Request method** : `post`
- **New Route**: `/booking`

### 2. updateBooking
- **Old Route**: `/api/app/booking/updateBooking`
- **Request method** : `put`
- **New Route**: `/booking`

### 3. cancelBooking
- **Old Route**: `/api/app/booking/cancelBooking`
- **New Route**: `/booking/cancelbooking`


### 4. verifySlots
- **Old Route**: `/api/app/booking/verifyslots`
- **New Route**: `/booking/verifyslots`

### 5. myBookings
- **Old Route**: `/api/app/booking/mybookings`
- **New Route**: `/booking/user/mybookings`

    **Query Parameters**:
  - `status` - booked/pending/cancelled

### 6. latestBookings
- **Old Route**: `/api/app/booking/allBookings`
- **New Route**: `/booking/user/latestbookings`

## 

### 1. authMapToken
- **Old Route**: `/api/app/booking/allBookings`
- **New Route**: `/setting/authmaptoken`

### 2. paymentkey
- **Old Route**: `/api/app/paymentkey`
- **New Route**: `/setting/paymentkey`

### 3. getTermsAndConditionPage
- **Old Route**: `/api/app/page/getPage?search=terms-and-conditions`
- **New Route**: `/pages/getpage?search=terms-and-conditions`

## Admin

### Service

### 1. updateService
- **Old Route**: `/api/app/ground/updateService`
- **Request method** : `put`
- **New Route**: `/service`

### 2. deleteService
- **Old Route**: `/api/app/ground/deleteService`
- **Request method** : `delete`
- **New Route**: `/service`
  
  **Query Parameters**:
  - `service_id` 


### Sports

### 1. updateSports
- **Old Route**: `/api/app/ground/updateService`
- **Request method** : `put`
- **New Route**: `/sports`

### 2. deleteSports
- **Old Route**: `/api/app/ground/updateService`
- **Request method** : `delete`
- **New Route**: `/sports`
  
  **Query Parameters**:
  - `sports_id` 

### Dashboard

### 1. adminDashboard
- **Old Route**: `/api/app/admin/dashboard`
- **New Route**: `/dashboard/admin


### User & Owner list

### 1. ownerList
- **Old Route**: `/api/app/user/ownerList`
- **New Route**: `/user/ownerlist`

  **Query Parameters**:
  - `page`
  - `search` - search with user lists

### 2. userList
- **Old Route**: `/api/app/user/userList`
- **New Route**: `/user/list`

  **Query Parameters**:
  - `page`
  - `search` - search with user lists

### Paymentkeys

### 1. getPaymentKey
- **Old Route**: `/api/app/getPaymentKey/:id`
- **New Route**: `/setting/getpaymentkey/:id`

### 2. savePaymentKey
- **Old Route**: `/api/app/savePaymentKey`
- **New Route**: `/setting/savepaymentkey`

### EmailPattern

### 1. getSingleEmailPattern
- **Old Route**: `/api/app/email/getSingleEmailPattern?name=`
- **New Route**: `/emailpattern/single?name=`

### 2. updateEmailPattern
- **Old Route**: `/api/app/email/updateEmailPattern`
- **New Route**: `/emailpattern/update`

### 3. getAllEmailPatterns
- **Old Route**: `/api/app/email/getEmailPatternList`
- **New Route**: `/emailpattern/list`
### 4. createEmailPatterns
- **Old Route**: `/api/app/email/createEmailPattern`
- **New Route**: `/emailpattern/create`

### Pages

### 1. updatepage
- **Old Route**: `/api/app/page/updatePage`
- **New Route**: `/pages/savepage`

### 2. getOnePageBySearch
- **Old Route**: `/api/app/page/getPage`
- **New Route**: `/pages/getpage?search=terms-and-conditions`

### 3. getAllPages
- **Old Route**: `/api/app/page/getAllpage`
- **New Route**: `/pages/getallpages`

### getAdminlogin
- **Old Route**: `/api/app/user/getadminlogin`
- **New Route**: `/user/getadminlogin`

 

