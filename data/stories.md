## happy path
* greet
  - utter_greet

## path1 all yes
* corona_assess{"corona":"coronavirus"}
  - utter_intial_bot
* decision{"decision_type":"Accept"}
  - utter_choose_city
* city_choice{"city":"Hyderabad","city":"Delhi","city":"Bihar","city":"Mumbai"}
  - utter_covid_check
* affirm{"result_type":"Yes"}
  - utter_covid_result
* affirm{"result_type":"Yes"}
  - utter_covid_positive
* affirm{"result_type":"Yes"}
  - utter_covid_recover
* affirm{"result_type":"Yes"}
  - utter_experience

## path1 all yes end no
* corona_assess{"corona":"coronavirus"}
  - utter_intial_bot
* decision{"decision_type":"Accept"}
  - utter_choose_city
* city_choice{"city":"Hyderabad","city":"Delhi","city":"Bihar","city":"Mumbai"}
  - utter_covid_check
* affirm{"result_type":"Yes"}
  - utter_covid_result
* affirm{"result_type":"Yes"}
  - utter_covid_positive
* affirm{"result_type":"Yes"}
  - utter_covid_recover
* deny{"result_type":"No"}
  - utter_assist

## path1 all yes end 2nos
* corona_assess{"corona":"coronavirus"}
  - utter_intial_bot
* decision{"decision_type":"Accept"}
  - utter_choose_city
* city_choice{"city":"Hyderabad","city":"Delhi","city":"Bihar","city":"Mumbai"}
  - utter_covid_check
* affirm{"result_type":"Yes"}
  - utter_covid_result
* affirm{"result_type":"Yes"}
  - utter_covid_positive
* deny{"result_type":"No"}
  - utter_stayathome

## path2 no yes
* corona_assess{"corona":"coronavirus"}
  - utter_intial_bot
* decision{"decision_type":"Accept"}
  - utter_choose_city
* city_choice{"city":"Hyderabad","city":"Delhi","city":"Bihar","city":"Mumbai"}
  - utter_covid_check
* deny{"result_type":"No"}
  - utter_choose_country
* affirm{"result_type":"Yes"}
  - utter_covid_symptoms
* affirm{"result_type":"Yes"}
  - utter_covid_breathe
* affirm{"result_type":"Yes","result_type":"No"}
  - utter_assist

## path2 no no
* corona_assess{"corona":"coronavirus"}
  - utter_intial_bot
* decision{"decision_type":"Accept"}
  - utter_choose_city
* city_choice{"city":"Hyderabad","city":"Delhi","city":"Bihar","city":"Mumbai"}
  - utter_covid_check
* deny{"result_type":"No"}
  - utter_choose_country
* deny{"result_type":"No"}
  - utter_covid_contacttrace
* affirm{"result_type":"Yes"}
  - utter_covid_symptoms
* affirm{"result_type":"Yes"}
  - utter_covid_breathe
* deny{"result_type":"Yes","result_type":"No"}
  - utter_assist

## path2 no no
* corona_assess{"corona":"coronavirus"}
  - utter_intial_bot
* decision{"decision_type":"Accept"}
  - utter_choose_city
* city_choice{"city":"Hyderabad","city":"Delhi","city":"Bihar","city":"Mumbai"}
  - utter_covid_check
* deny{"result_type":"No"}
  - utter_choose_country
* deny{"result_type":"No"}
  - utter_covid_contacttrace
* deny{"result_type":"No"}
  - utter_aint_travelled

<!-- * mood_great
  - utter_happy

## sad path 1
* greet
  - utter_greet
* mood_unhappy
  - utter_cheer_up
  - utter_did_that_help
* affirm
  - utter_happy

## sad path 2
* greet
  - utter_greet
* mood_unhappy
  - utter_cheer_up
  - utter_did_that_help
* deny
  - utter_goodbye

## say goodbye
* goodbye
  - utter_goodbye

## bot challenge
* bot_challenge
  - utter_iamabot -->
