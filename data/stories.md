## happy path
* greet
  - utter_greet
* positive
    - utter_positive  
* chitchat_creativeorchards
  - utter_chitchat_creativeorchards
* chitchat_identity
  - utter_chitchat_identity  
* chitchat_pricing
  - utter_chitchat_pricing
* chitchat_smart_assistant
  - utter_chitchat_smart_assistant
* request_contact
  - form_contact
  - form{"name":"form_contact"}
  - form{"name":null} 
  - utter_noworries

## thank you
* thankyou
  - utter_thankyou

## tell a joke
* joke
  - utter_joke_intro
  - utter_joke
  - utter_laugh   
* affirm
  - form_contact
* deny 
  - utter_bye

## api path

* demo_1
  - action_selektor

## sapi

* sapi
  - action_sapi

## New Story

* greet
    - utter_greet
* positive
    - form_contact
    - form{"name":"form_contact"}
    - slot{"requested_slot":"email"}
* positive{"email":"kkiarie4@gmail.com"}
    - slot{"email":"kkiarie4@gmail.com"}
    - form_contact
    - slot{"email":"kkiarie4@gmail.com"}
    - slot{"requested_slot":"phone-number"}
* demo_1{"phone-number":"(+25) 4715295492"}
    - slot{"phone-number":"(+25) 4715295492"}
    - form_contact
    - slot{"phone-number":"(+25) 4715295492"}
    - slot{"requested_slot":"time"}
* deny{"time":"2020-10-16T00:00:00.000+03:00"}
    - slot{"time":"2020-10-16T00:00:00.000+03:00"}
    - form_contact
    - slot{"time":"2020-10-16T00:00:00.000+03:00"}
    - form{"name":null}
    - slot{"requested_slot":null}
    - utter_noworries

## New Story

* greet
    - utter_greet
* thankyou
    - utter_thankyou
* thankyou
    - utter_thankyou
* greet
    - utter_greet
* positive
    - utter_positive

## New Story

* request_contact
    - form_contact
    - form{"name":"form_contact"}
    - slot{"requested_slot":"email"}
* positive{"email":"kkiarie4@gmail.com"}
    - slot{"email":"kkiarie4@gmail.com"}
    - form_contact
    - slot{"email":"kkiarie4@gmail.com"}
    - slot{"requested_slot":"phone-number"}
* chitchat_identity
    - utter_chitchat_identity
* chitchat_smart_assistant{"phone-number":"(+25) 4715295492"}
    - slot{"phone-number":"(+25) 4715295492"}
    - form_contact
    - slot{"phone-number":"(+25) 4715295492"}
    - slot{"requested_slot":"time"}
* greet{"time":"2020-10-14T00:00:00.000+03:00"}
    - slot{"time":"2020-10-14T00:00:00.000+03:00"}
    - form_contact
    - slot{"time":"2020-10-14T00:00:00.000+03:00"}
    - form{"name":null}
    - slot{"requested_slot":null}
    - utter_noworries

## demo request booking

* greet
  - utter_greet
* request_booking
  - form_booking
  - form{"name":"form_booking"}
  - form{"name":null} 
  - utter_noworries_booking

## Demo Booking Happy Path

* greet
    - utter_greet
* request_booking
    - form_booking
    - form{"name":"form_booking"}
    - slot{"requested_slot":"my_service"}
* inform{"my_service":"salon"}
    - slot{"my_service":"salon"}
    - form_booking
    - slot{"my_service":"salon"}
    - slot{"requested_slot":"number"}
* chitchat_creativeorchards{"number":2}
    - slot{"number":2}
    - form_booking
    - slot{"number":2}
    - slot{"requested_slot":"phone-number"}
* goodbye{"phone-number":"(+25) 4715295492"}
    - slot{"phone-number":"(+25) 4715295492"}
    - form_booking
    - slot{"phone-number":"(+25) 4715295492"}
    - slot{"requested_slot":"time"}
* deny{"time":"2020-10-14T10:00:00.000+03:00"}
    - slot{"time":"2020-10-14T10:00:00.000+03:00"}
    - form_booking
    - slot{"time":"2020-10-14T10:00:00.000+03:00"}
    - form{"name":null}
    - slot{"requested_slot":null}
    - utter_noworries_booking
