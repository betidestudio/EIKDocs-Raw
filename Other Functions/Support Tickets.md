# Support Tickets

!!!info At the end of the page there is documentation for structures and enumerations

### Set Up Support Tickets With Your Game

Fist you need an api key found in EOSDevPortal->YourProduct->GameServices->Ticketing->ShowAPIKey. Then paste this key in the field called Api Key in EIK configuration in Unreal Engines settings panel. 

You are now good to go!

## Sending Support Ticket

To send a support ticket players need to fill out the *SupportTicketData* structure and then you will call the function to send the ticket. You will reccive all tickets on eos backend, and will be able to respond to them there. The player sending the ticket will continue the conversation in their mailbox.

### Sending Support Ticket Input Parameters

`TicketData` Struct of type *SupportTicketData*

### Sending Support Ticket Return Values

`Response Code` Result code, *200* ok, *400* error

`Response Data` Struct of type *SupportTicketResponseData* containing response information from eos

`Response String` A response string containing any errors

---

## Exporting User Data

To comply with gdpr you need to give the user the option to delete and export their data. Exportning data is done with *Export EIK Support Ticket Data*.

### Exporting User Data Input Parameters

`Email` The users email in string format

### Exporting User Data Return Values

`Response Code` Result code, *200* ok, *400* error

`ConversationData` An array of structs of type *ConversationData* containing converation data stored on eos

`Response String` A response string containing any errors

---

## Delete EIK Support Ticket Data

To delete a users support ticket data you need to call *Delete EIK Support Ticket Data*.

### Delete EIK Support Ticket Data Input Parameters

`Email` The users email in string format

### Delete EIK Support Ticket Data Return Values

`Response Code` Result code, *200* ok, *400* error

`WasSuccessful` A boolean indicating success if true. 

`Response String` A response string containing any errors

---

### Structures
---
#### `SupportTicketData`

    Enum ESupportTicketSubject: Subject

    String: Message

    String: SenderEmail

    String: SenderName

    String: Guid, the unique identifier for a user

    String: ErrorCode

    String: SystemOS

    String: SystemAntiMalware
    
    String: SystemOther
---
#### `SupportTicketResponseData`

    String: prod_name

    String: prod_slug

    String: guid

    String: sender_name

    String: sender_email

    String: subject

    String: message

    String: error_code

    String: system_os

    String: system_antimalware

    String: system_other

    String: timestamp
---
#### `ConversationData`

    String: Guid

    String: Subject

    String: Message

    String: SenderName

    String: SenderEmail

    String: Timestamp

    Array, struct: MessageData Messages
---
#### `MessageData`

    Integer: TicketId

    String: Message

    String: SenderName
    
    String: SenderEmail
    
    String: Timestamp
---

### Enumerations
---
#### `ESupportTicketSubject`

    ST_open_question
    ST_technical_support
    ST_ban_appeal
---