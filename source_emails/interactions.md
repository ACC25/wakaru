## Interactions for Wakaru Source Emails

### Fictional Company Information

+ Name: Wakaru
+ Description: Company that specializes in surfboards
+ Products: Surfboard repairs, building surf boards, purchasing pre-built surfboards, surf accessories and wetsuits

### Interaction Pattern

Each email chain will have four messages:

+ First: customer's initial query (starting at the bottom of the template)
+ Second: company's initial response
+ Third: customer provides contextual information to support query
+ Fourth: company closes ticket by granting or denying request, and provides reasoning (ending at the top of the template)
  + for `good` templates, reasoning is expected  
  + For `bad` templates, excluding reasoning is a legitimate tactic for increasing negative tone

#### Source Organization

Emails will be sorted, based on their subject line, into three categories upon receipt:

+ `denying_request_bad`
+ `denying_request_good`
+ `granting_request_good`

Based on this study (link here), there is a larger statistical difference in how customers perceive tonnage based on whether their request is denied or granted vs general tonnage across all interactions, so the goal of the source emails is to help highlight the tonnage of denying/granting interactions. For instance, we are ignoring `granting_request_bad` emails because customers would not necessarily care what the tonnage is if they are getting what they want. Based on time constraints, it is more useful to quantify the tonnage of interactions that we know customers will likely find more impactful on their overall experience.

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
