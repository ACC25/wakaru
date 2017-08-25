## Interactions for Wakaru Source Data

### Fictional Company Information

+ Name: Wakaru
+ Description: Company that specializes in surfboards
+ Products: Surfboard repairs, building surf boards, purchasing pre-built surfboards, surf accessories and wetsuits

### Definitions

+ `public result` refers to the result from the google form, submitted by an anonymous volunteer, which is designed to `loosely` mimic an email conversation between a customer and customer service representative
+ `private result` refers to the result from the google form, submitted by an approved source, which is designed to `closely` mimic a real conversation between a customer and customer service representative
+ `professional result` refers to the result from the google form, submitted by an approved source, which is a `exact` copy of a real world answer by a customer service professional

### Interaction Pattern

Each form will have two messages:

+ First: customer's query
+ Second: company's response
  + for `good` responses, reasoning is expected  
  + For `bad` responses, excluding reasoning is a legitimate tactic for increasing negative tone

### Source Weight

+ `public results` will be weighed TBD%
+ `private results` will be weighed TBD%

### Source Organization

Public results will be sorted into three categories upon receipt:

+ `denying_request_bad`
+ `denying_request_good`
+ `granting_request_good`

### Source Forms

#### Public result forms

###### Wait Time Queries
+ [wait_time_granting_request_good](https://docs.google.com/forms/d/e/1FAIpQLScrN67IPdkUv_HCQsrNt5OA9MAqXBdxlpV_7wTNH-bbh6OcVw/viewform)
+ [wait_time_denying_request_good](https://docs.google.com/forms/d/e/1FAIpQLSegBjxlyDbalSR8Mp56KwOAGxPDZUIorPCoyzNqsAexfnWiyA/viewform)
+ [wait_time_denying_request_bad](https://docs.google.com/forms/d/e/1FAIpQLSfvcDyT7WjE-XCUEZc1uWti9C164Uq-qc4vcgIr1T0ztz_ppQ/viewform)
###### Warranty Queries
+ [warranty_granting_request_good](https://docs.google.com/forms/d/e/1FAIpQLSf91Frgs0fGr5XYD2wHj1gzKaTWRObGPydHm_sS-UMgN3iQYQ/viewform)
+ [warranty_denying_request_good](https://docs.google.com/forms/d/e/1FAIpQLSfeF0wD6bRT2IT8zqyMVl1jf6fVfNZ0qgDEDxcwD1tEaLb-Og/viewform)
+ [warranty_denying_request_bad](https://docs.google.com/forms/d/e/1FAIpQLScl-QX2IaLG3-EZkCDtad238I-n9kov21G1CufpFvrmnQKrVw/viewform)

#### Private result forms

###### TBD

###### TBD

### Source Form Prompts

###### Wait Time Queries
+ [wait_time_granting_request_good](https://gist.github.com/ACC25/afc46f97a452066066de3d81d92b3b09)
+ [wait_time_denying_request_good](https://gist.github.com/ACC25/fb92ef1830633fc0e685dcf7f151e1d4)
+ [wait_time_denying_request_bad](https://gist.github.com/ACC25/9ff0d79cb34a32e9a07459759d12af5c)
###### Warranty Queries
+ [warranty_granting_request_good](https://gist.github.com/ACC25/40b81154cd968225beaf37bd61606097)
+ [warranty_denying_request_good](https://gist.github.com/ACC25/0200d775b4efc996e3200ba1e19b4464)
+ [warranty_denying_request_bad](https://gist.github.com/ACC25/ebf6aa3bb0905f0cce3397f75fd4f46b)


Based on this study (link here), there is a larger statistical difference in how customers perceive tone based on whether their request is denied or granted vs general tonnage across all interactions, so the goal of the source emails is to help highlight the tone of denying/granting interactions. For instance, we are ignoring `granting_request_bad` emails because customers would not necessarily care what the tone is if they are getting what they want. Based on time constraints, it is more useful to quantify the tone of interactions that we know customers will likely find more impactful on their overall experience.

### Possible interactions

#### Surfboards

+ Querying inventory on already built boards
+ Querying wait times for building a board
+ Querying materials used for building a board
+ Querying wait times for surfboard repairs
+ Querying warranty policy

#### Accessories

+ Querying inventory on accessories
+ Querying materials used on a particular accessory
+ Querying warranty policy

#### wetsuits

+ Querying clothing inventory sizes for a specific article
+ Querying materials used on a particular article
+ Querying warranty policy
