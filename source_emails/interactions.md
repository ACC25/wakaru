## Interactions for Wakaru Source Emails

### Basic Information

+ Name: Wakaru
+ Description: Company that specializes in surfboards
+ Products: Surfboard repairs, building surf boards, purchasing pre-built surfboards, surf accessories and wetsuits

### Interaction Pattern

Each email chain will have four messages:

+ First: customer's initial query
+ Second: company's initial response
+ Third: customer provides contextual information to support query
+ Fourth: company closes ticket by granting or denying request, and provides reasoning
  + for `good` templates, reasoning is expected  
  + For `bad` templates, excluding reasoning is a legitimate tactic for increasing negative tone

Based on the article (link here), there is a larger statistical difference between how customers perceive tonnage based on whether their request is denied or granted, so the goal of the source emails is to help highlight the tonnage of denying/granting interactions. For instance, we are ignoring `granting_request_bad` emails because, according to the study, customers would not necessarily care what the tonnage is if they are getting what they want. Based on time constraints, it is more useful to quantify the tonnage of interactions that we know customers will like or dislike.

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
