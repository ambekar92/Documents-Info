# API Documentation

## Index

1. **API Endpoints**
   - [Get Customer List](#get-customer-list)
   - [Get Order Schedule Booking List](#get-order-schedule-booking-list)
   - [Get Costing Sheet List](#get-costing-sheet-list)
   - [Get Dispatch Docs List](#get-dispatch-docs-list)
   - [Get IOM Credit Note List](#get-iom-credit-note-list)
   - [Get Toll Master List](#get-toll-master-list)
   - [Get Credit Policy List](#get-credit-policy-list)
   - [Get Credit Policy Detail](#get-credit-policy-detail)
   - [Get Fully Dispatched Order Booking List](#get-fully-dispatched-order-booking-list)
   - [Get Order Schedule SO List](#get-order-schedule-so-list)
   - [Get Order Status for Chart](#get-order-status-for-chart)
   - [Chart API for Order](#chart-api-for-order)
   - [Chart API for CARDS](#chart-api-for-cards)
   - [Cancel Order](#cancel-order)
   - [Carry Forward Order](#carry-forward-order)
   - [Get PO List](#get-po-list)
   - [Get Customer Detail](#get-customer-detail)
   - [Get Quotation Detail](#get-quotation-detail)
   - [Get Costing Sheet Detail](#get-costing-sheet-detail)
   - [Get Dispatch Detail](#get-dispatch-detail)
   - [Add Order Schedule Booking](#add-order-schedule-booking)
   - [Add Customer API](#add-customer-api)
   - [Add TollMaster API](#add-tollmaster-api)
   - [Add Credit Policy](#add-credit-policy)
   - [Update/Edit TollMaster API](#updateedit-tollmaster-api)
   - [Delete TollMaster API](#delete-tollmaster-api)
   - [Get Customers Dropdown API](#get-customers-dropdown-api)
   - [Get ProjectName Dropdown API](#get-projectname-dropdown-api)
   - [Get Route Number Dropdown API](#get-route-number-dropdown-api)
   - [Get Route Number Detail API](#get-route-number-detail-api)
   - [Update Customer KYC API](#update-customer-kyc-api)
   - [Update/Edit Customer API](#updateedit-customer-api)
   - [Add Costing Sheet](#add-costing-sheet)
   - [Add Dispatch](#add-dispatch)
   - [Update Dispatch Confirm Status](#update-dispatch-confirm-status)
   - [Update Dispatch Invoice Detail](#update-dispatch-invoice-detail)
   - [Add Quotation API](#add-quotation-api)



### Get Customer List
**Method:** POST  
**Endpoint:** `/customer/api/generateCustomerQuery`  
**Request Body:**
```json
{
    "queryName": "getCustomerListV1",
    "module":"CUSTOMER",
    "page": 1,
    "per_page": 10,
    "searchTerm":""
}
```

---

### Get Order Schedule Booking List
**Method:** POST  
**Endpoint:** `/customer/api/generateCustomerQuery`  
**Request Body:**
```json
{
    "queryName": "getOrderScheduleBookingList",
    "module": "CUSTOMER",
    "page": 1,
    "per_page": 10,
    "searchTerm": ""
}
```

---

### Get Costing Sheet List
**Method:** POST  
**Endpoint:** `/customer/api/generateCustomerQuery`  
**Request Body:**
```json
{
    "queryName": "getCostingSheetList",
    "module":"COSTING_SHEET",
    "page": 1,
    "per_page": 10,
    "searchTerm":""
}
```

---

### Get Dispatch Docs List
**Method:** POST  
**Endpoint:** `/customer/api/generateCustomerQuery`  
**Request Body:**
```json
{
    "queryName": "getDispatchDocList",
    "module":"DISPATCH",
    "page": 1,
    "per_page": 10,
    "searchTerm":""
}
```

---

### Get IOM Credit Note List
**Method:** POST  
**Endpoint:** `/customer/api/generateCustomerQuery`  
**Request Body:**
```json
{
    "queryName" : "IOMCreditNote",
    "module":"",
    "page": 1,
    "per_page": 10,
    "searchTerm":""
}
```

---

### Get Toll Master List
**Method:** POST  
**Endpoint:** `/customer/api/generateCustomerQuery`  
**Request Body:**
```json
{
    "queryName": "GetTollMasterList",
    "module":"",
    "page": 1,
    "per_page": 10,
    "searchTerm":""
}
```

---

### Get Credit Policy List
**Method:** POST  
**Endpoint:** `/customer/api/generateCustomerQuery`  
**Request Body:**
```json
{
    "queryName": "getCreditPolicyList",
    "module":"CUSTOMER_CREDIT_POLICY",
    "page": 1,
    "per_page": 10,
    "searchTerm":""
}
```

---

### Get Credit Policy Detail
**Method:** POST  
**Endpoint:** `/customer-v1/api/getCreditPolicyDetail`  
**Request Body:**
```json
{
    "documentNumber": "CL0008"
}
```

---

### Get Fully Dispatched Order Booking List
**Method:** POST  
**Endpoint:** `/customer/api/generateCustomerQuery`  
**Request Body:**
```json
{
    "queryName": "getFullyDispatchedOrderBookingList",
    "module":"",
    "page": 1,
    "per_page": 10,
    "searchTerm":""
}
```

---

### Get Order Schedule SO List
**Method:** POST  
**Endpoint:** `/customer/api/generateCustomerQuery`  
**Request Body:**
```json
{
    "queryName": "getOrderScheduleSOList",
    "module":"",
    "page": 1,
    "per_page": 10,
    "searchTerm":""
}
```

---

### Get Order Status for Chart
**Method:** POST  
**Endpoint:** `/customer/api/generateCustomerChartQuery`  
**Request Body:**
```json
{
    "queryName": "Order_StatusChartList",
    "chartCategory": "orderStatus"
}
```

---

### Chart API for Order
**Method:** POST  
**Endpoint:** `/customer-v1/api/dashboard`  
**Request Body:**
```json
{
    "module":"order",
    "action":"Custom",  
    "month": "02",
    "year": 2025,
    "fromDate":"2025-01-01",
    "toDate":"2025-02-12"
}
```

---

### Chart API for CARDS
**Method:** POST  
**Endpoint:** `/customer-v1/api/ChartCountCard`  
**Request Body Examples:**
```json
{
    "queryName": "GetTotalOrderCount",
    "month": "02",
    "year": 2025
}
```
```json
{
    "queryName": "totalConfirmedDispatchCount",
    "month": "02",
    "year": 2025
}
```
```json
{
    "queryName": "totalOrderCompletedCount",
    "month": "02",
    "year": 2025
}
```
```json
{
    "queryName": "totalCustomerCount",
    "month": "02",
    "year": 2025
}
```

---

### Cancel Order
**Method:** POST  
**Endpoint:** `/customer-v1/api/cancelOrder`  
**Request Body:**
```json
{
    "orderSchedulingNr": "ORD0018",
    "orderStatus": "Cancelled",
    "balOrderQuantityLoad": 1,
    "cancelledOrderQuantityLoad": 1,
    "cancelledOrderRemarks": "Cancelled for over load"
}
```

---

### Carry Forward Order
**Method:** POST  
**Endpoint:** `/customer-v1/api/carryForwardOrder`  
**Request Body:**
```json
{
    "orderSchedulingNr": "ORD0030",
    "carryForwardOrderLoad": 1,
    "dispatchDate": "2025-02-20"
}
```

### Get Toll Master List
- **Method:** POST
- **Endpoint:** `/customer/api/generateCustomerQuery`
- **Request Body:**
  ```json
  {
    "queryName": "getCustomerTollMaster",
    "module": "TOLL",
    "page": 1,
    "per_page": 10,
    "searchTerm": ""
  }
  ```

### Get PO List
- **Method:** POST
- **Endpoint:** `/customer/api/generateCustomerQuery`
- **Request Body:**
  ```json
  {
    "queryName": "getPOListV1",
    "module": "PO",
    "page": 1,
    "per_page": 10,
    "searchTerm": ""
  }
  ```

### Get Customer Detail
- **Method:** POST
- **Endpoint:** `/customer-v1/api/getCustomerDetail`
- **Request Body:**
  ```json
  {
    "documentNumber": "ADMIN"
  }
  ```

### Get Quotation Detail
- **Method:** POST
- **Endpoint:** `/customer-v1/api/getQuotationDetail`
- **Request Body:**
  ```json
  {
    "documentNumber": "Q0019"
  }
  ```

### Get Costing Sheet Detail
- **Method:** POST
- **Endpoint:** `/customer-v1/api/getCostingSheetDetail`
- **Request Body:**
  ```json
  {
    "documentNumber": "CS0027"
  }
  ```

### Get Dispatch Detail
- **Method:** POST
- **Endpoint:** `/customer-v1/api/getDispatchDetail`
- **Request Body:**
  ```json
  {
    "documentNumber": "DIS0001"
  }
  ```

### Add Order Schedule Booking
- **Method:** POST
- **Endpoint:** `/customer-v1/api/addOrderScheduleBooking`
- **Request Body:**
  ```json
  {
    "data": [{},{}]
  }
  ```

### Add Customer API
- **Method:** POST
- **Endpoint:** `/customer-v1/api/addCustomer`
- **Request Body:**
  ```json
  {
    "data": {}
  }
  ```
- **Redirect URL:** [Customer Register](http://localhost:3000/customer-register)

### Add TollMaster API
- **Method:** POST
- **Endpoint:** `/customer-v1/api/addTollMaster`
- **Request Body:**
  ```json
  {
    "data": {}
  }
  ```

### Add Credit Policy
- **Method:** POST
- **Endpoint:** `/customer-v1/api/addCreditPolicy`
- **Request Body:**
  ```json
  {
    "data": {}
  }
  ```

### Update/Edit TollMaster API
- **Method:** POST
- **Endpoint:** `/customer-v1/api/updateTollMaster`
- **Request Body:**
  ```json
  {
    "tollNumber": "10",
    "routeNumber": "3",
    "routeDescription": "Free zone-1"
  }
  ```

### Delete TollMaster API
- **Method:** POST
- **Endpoint:** `/customer-v1/api/deleteTollMaster`
- **Request Body:**
  ```json
  {
    "tollNumber": "0"
  }
  ```

### Get Customers Dropdown API
- **Method:** POST
- **Endpoint:** `/customer-v1/api/getCustomers`
- **Request Body:**
  ```json
  {}
  ```

### Get ProjectName Dropdown API
- **Method:** POST
- **Endpoint:** `/customer-v1/api/getProjectName`
- **Request Body:**
  ```json
  {
    "userId": "C0082"
  }
  ```

### Get Route Number Dropdown API
- **Method:** POST
- **Endpoint:** `/customer-v1/api/getRouteNumber`
- **Request Body:**
  ```json
  {}
  ```

### Get Route Number Detail API
- **Method:** POST
- **Endpoint:** `/customer-v1/api/getRouteNumberDetail`
- **Request Body:**
  ```json
  {
    "routeNumber": "2"
  }
  ```

### Update Customer KYC API
- **Method:** POST
- **Endpoint:** `/customer-v1/api/updateKYCCustomer`
- **Request Body:**
  ```json
  {
    "userId": "C0082",
    "organisationName": "Yukta T Swamy",
    "firstName": "Yukta T Swamy"
  }
  ```

### Update/Edit Customer API
- **Method:** POST
- **Endpoint:** `/customer-v1/api/updateCustomer`
- **Request Body:**
  ```json
  {
    "userId": "C0062",
    "organisationName": "Yukta T Swamy",
    "firstName": "Yukta T Swamy"
  }
  ```
- **Redirect URL:** [Customer Register Detail](http://localhost:3000/customer-register-detail)

### Add Costing Sheet
- **Method:** POST
- **Endpoint:** `/customer-v1/api/addCostingSheet`
- **Request Body:**
  ```json
  {
    "data": {}
  }
  ```
- **Redirect URL:** [Costing Sheet](http://localhost:3000/costing-sheet)

### Add Dispatch
- **Method:** POST
- **Endpoint:** `/customer-v1/api/addDispatch`
- **Request Body:**
  ```json
  {
    "data": {}
  }
  ```

### Update Dispatch Confirm Status
- **Method:** POST
- **Endpoint:** `/customer-v1/api/updateDispatchConfirm`
- **Request Body:**
  ```json
  {
    "dispatchDocNr": "DIS0050",
    "dispatchStatus": "Confirmed"
  }
  ```

### Update Dispatch Invoice Detail
- **Method:** POST
- **Endpoint:** `/customer-v1/api/updateDispatchInvoice`
- **Request Body:**
  ```json
  {
    "dispatchDocNr": "DIS0088",
    "dispInvoiceNumber": "2440014668",
    "dispInvoiceDate": "02.01.2025",
    "dispTotalAmount": 40332,
    "dispDescription": "MFG. Plaster Sand (0-2.36mm)"
  }
  ```

### Add Quotation API
- **Method:** POST
- **Endpoint:** `/customer-v1/api/addQuotation`
- **Request Body:**
  ```json
  {
    "data": {}
  }
  ```

### Update Sales Document Number
- **Method:** POST
- **Endpoint:** `/customer-v1/api/updateSalesDocumentNr`
- **Request Body:**
  ```json
  {
    "orderSchedulingNr": "ORD0108",
    "salesDocumentNr": "S0001"
  }
  ```



---

*(More APIs can be added in the same format.)*

