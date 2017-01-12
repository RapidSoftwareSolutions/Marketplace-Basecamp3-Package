# Basecamp3 Package

* Domain: 
* Credentials: clientId, clientSecret

## How to get credentials: 
0. Go to https://integrate.37signals.com/
1. Click on **Register application** button
2. In `Integration` list choose Basecamp 3. In addition, fill infromation about your app. Press **Register this app** button
3. Copy and save your `Client ID`, `Client Secret`, `Redirect URI`
4. Direct user to https://launchpad.37signals.com/authorization/new?client_id=CLIENT_ID&redirect_uri=REDIRECT_URI&type=web_server
5. If the user accepts, they will be redirected back to https://[your registered redirect URI]/?code=[CODE]
6. Use **getAccessToken** method to get users's accessToken.

## Basecamp3. 
Create an attachment

| Field        | Type  | Description
|--------------|-------|----------
| accountId    | String| Basecamp Account ID.
| accessToken  | String| OAuth2 Access Token from `getAccessToken` block.
| name         | String| File name.
| file         | File  | File to upload

## Basecamp3.getBasecamps
 Returns a list of active Basecamps visible to the current user sorted by most recently created Basecamp first.

| Field        | Type  | Description
|--------------|-------|----------
| accountId    | String| Basecamp Account ID.
| accessToken  | String| OAuth2 Access Token from `getAccessToken` block.
| status       | String| When set to `archived` or `trashed`, will return archived or trashed Basecamps visible to the current user.

## Basecamp3.getSingleBasecamp
Returns the Basecamp with the given ID, granted they have access to it.

| Field        | Type  | Description
|--------------|-------|----------
| accountId    | String| Basecamp Account ID.
| accessToken  | String| OAuth2 Access Token from `getAccessToken` block.
| id           | String| Basecamp ID

## Basecamp3.createBasecamp
Creates a new Basecamp.

| Field        | Type  | Description
|--------------|-------|----------
| accountId    | String| Basecamp Account ID.
| accessToken  | String| OAuth2 Access Token from `getAccessToken` block.
| name         | String| Basecamp name.
| description  | String| Basecamp description.

## Basecamp3.updateBasecamp
Will allow updating of a Basecamp's name and description.

| Field        | Type  | Description
|--------------|-------|----------
| accountId    | String| Basecamp Account ID.
| accessToken  | String| OAuth2 Access Token from `getAccessToken` block.
| id           | String| Basecamp ID.
| name         | String| New Basecamp name.
| description  | String| New Basecamp description.

## Basecamp3.deleteBasecamp
Will mark the Basecamp with the given ID as trashed.

| Field        | Type  | Description
|--------------|-------|----------
| accountId    | String| Basecamp Account ID.
| accessToken  | String| OAuth2 Access Token from `getAccessToken` block.
| id           | String| Basecamp ID.

## Basecamp3.getCampfires
Returns a list of all active Campfires visible to the current user.

| Field        | Type  | Description
|--------------|-------|----------
| accountId    | String| Basecamp Account ID.
| accessToken  | String| OAuth2 Access Token from `getAccessToken` block.

## Basecamp3.getSingleCampfire
Return the Campfire with ID `campfireId` in the Basecamp with ID `basecampId`.

| Field        | Type  | Description
|--------------|-------|----------
| accountId    | String| Basecamp Account ID.
| accessToken  | String| OAuth2 Access Token from `getAccessToken` block.
| basecampId   | String| Basecamp ID.
| campfireId   | String| Campfire ID.

## Basecamp3.getCampfireLines
Returns a list of Campfire lines of the Campfire with ID `campfireId` in the Basecamp with ID `basecampId`

| Field        | Type  | Description
|--------------|-------|----------
| accountId    | String| Basecamp Account ID.
| accessToken  | String| OAuth2 Access Token from `getAccessToken` block.
| basecampId   | String| Basecamp ID.
| campfireId   | String| Campfire ID.

## Basecamp3.getCampfireLine
Returns the Campfire line with ID `lineId` in the Campfire with ID `campfireId` in the Basecamp with ID `basecampId`.

| Field        | Type  | Description
|--------------|-------|----------
| accountId    | String| Basecamp Account ID.
| accessToken  | String| OAuth2 Access Token from `getAccessToken` block.
| basecampId   | String| Basecamp ID.
| campfireId   | String| Campfire ID.
| lineId       | String| Campfire Line ID.

## Basecamp3.createCampfireLine
Creates a line in the Campfire with ID `campfireId` in the Basecamp with ID `basecampId`.

| Field        | Type  | Description
|--------------|-------|----------
| accountId    | String| Basecamp Account ID.
| accessToken  | String| OAuth2 Access Token from `getAccessToken` block.
| basecampId   | String| Basecamp ID.
| campfireId   | String| Campfire ID.

## Basecamp3.getChatbots
Return all the chatbots from the account with the line URL for the campfire with id `campfireId` on the basecamp with an ID of `basecampId`.

| Field        | Type  | Description
|--------------|-------|----------
| accountId    | String| Basecamp Account ID.
| accessToken  | String| OAuth2 Access Token from `getAccessToken` block.
| basecampId   | String| Basecamp ID.
| campfireId   | String| Campfire ID.

## Basecamp3.getSingleChatbot
Returns the chatbot with an ID of `botId` with the line URL from the Basecamp with ID `basecampId`.

| Field        | Type  | Description
|--------------|-------|----------
| accountId    | String| Basecamp Account ID.
| accessToken  | String| OAuth2 Access Token from `getAccessToken` block.
| basecampId   | String| Basecamp ID.
| campfireId   | String| Campfire ID.
| botId        | String| Bot ID.

## Basecamp3.createChatbot
Creates a chatbot on the account and returns the new chatbot with the lines URL from the Basecamp with ID `basecampId`.

| Field        | Type  | Description
|--------------|-------|----------
| accountId    | String| Basecamp Account ID.
| accessToken  | String| OAuth2 Access Token from `getAccessToken` block.
| basecampId   | String| Basecamp ID.
| campfireId   | String| Campfire ID.
| serviceName  | String| Chatbot name, which will be used to invoke queries and commands on interactive bots.
| commandUrl   | String| HTTPS url that Basecamp should call when the bot is addressed

## Basecamp3.updateChatbot
Allows changing the service name and commandURL of the chatbot with an ID of `botId` in the Basecamp with ID `botId`.

| Field        | Type  | Description
|--------------|-------|----------
| accountId    | String| Basecamp Account ID.
| accessToken  | String| OAuth2 Access Token from `getAccessToken` block.
| basecampId   | String| Basecamp ID.
| campfireId   | String| Campfire ID.
| botId        | String| Bot ID.
| serviceName  | String| Chatbot name, which will be used to invoke queries and commands on interactive bots.
| commandUrl   | String| HTTPS url that Basecamp should call when the bot is addressed

## Basecamp3.deleteChatbot
Deletes the chatbot with an ID of `botId` across the account.

| Field        | Type  | Description
|--------------|-------|----------
| accountId    | String| Basecamp Account ID.
| accessToken  | String| OAuth2 Access Token from `getAccessToken` block.
| basecampId   | String| Basecamp ID.
| campfireId   | String| Campfire ID.
| botId        | String| Bot ID.

## Basecamp3.getClientApprovals
Returns a list of client approvals in the Basecamp with an ID of `basecampId`.

| Field        | Type  | Description
|--------------|-------|----------
| accountId    | String| Basecamp Account ID.
| accessToken  | String| OAuth2 Access Token from `getAccessToken` block.
| basecampId   | String| Basecamp ID.

## Basecamp3.getSingleClientApproval
Returns the client approval with an ID of `approvalId` in the Basecamp with an ID of `basecampId`.

| Field        | Type  | Description
|--------------|-------|----------
| accountId    | String| Basecamp Account ID.
| accessToken  | String| OAuth2 Access Token from `getAccessToken` block.
| basecampId   | String| Basecamp ID.
| approvalId   | String| Approval ID.

## Basecamp3.getClientCorrespondences
Returns a list of client correspondences in the Basecamp with an ID of `basecampId`.

| Field        | Type  | Description
|--------------|-------|----------
| accountId    | String| Basecamp Account ID.
| accessToken  | String| OAuth2 Access Token from `getAccessToken` block.
| basecampId   | String| Basecamp ID.

## Basecamp3.getSingleClientCorrespondence
return the client correspondence with an ID of `correspondenceId` in the Basecamp with an ID of `basecampId`.

| Field               | Type  | Description
|---------------------|-------|----------
| accountId           | String| Basecamp Account ID.
| accessToken         | String| OAuth2 Access Token from `getAccessToken` block.
| basecampId          | String| Basecamp ID.
| correspondenceId    | String| Correspondence ID.

## Basecamp3.getClientReplies
return a paginated list of client replies in the Basecamp with an ID of `basecampId` and the recording with ID of `recordingId`.

| Field        | Type  | Description
|--------------|-------|----------
| accountId    | String| Basecamp Account ID.
| accessToken  | String| OAuth2 Access Token from `getAccessToken` block.
| basecampId   | String| Basecamp ID.
| recordingId  | String| Recording ID.

## Basecamp3.getSingleClientReply
return the client reply with an ID of `replyId` for the recording with an ID of `recordingId` in the Basecamp with an ID of `basecampId`.

| Field        | Type  | Description
|--------------|-------|----------
| accountId    | String| Basecamp Account ID.
| accessToken  | String| OAuth2 Access Token from `getAccessToken` block.
| basecampId   | String| Basecamp ID.
| recordingId  | String| Recording ID.
| replyId      | String| Reply ID.

## Basecamp3.getComments
Return a list of active comments in the Basecamp with an ID of `basecampId` and the recording with ID of `recordingId`.

| Field        | Type  | Description
|--------------|-------|----------
| accountId    | String| Basecamp Account ID.
| accessToken  | String| OAuth2 Access Token from `getAccessToken` block.
| basecampId   | String| Basecamp ID.
| recordingId  | String| Recording ID.

## Basecamp3.getSingleComment
Returns the comment with an ID of `commentId` in the Basecamp with an ID of `basecampId`.

| Field        | Type  | Description
|--------------|-------|----------
| accountId    | String| Basecamp Account ID.
| accessToken  | String| OAuth2 Access Token from `getAccessToken` block.
| basecampId   | String| Basecamp ID.
| commentId    | String| Comment ID.

## Basecamp3.createComment
Publishes a comment in the Basecamp with ID `commentId` and under the recording with an ID of `recordingId`.

| Field        | Type  | Description
|--------------|-------|----------
| accountId    | String| Basecamp Account ID.
| accessToken  | String| OAuth2 Access Token from `getAccessToken` block.
| basecampId   | String| Basecamp ID.
| recordingId  | String| Recording ID.
| content      | String| The body of the messag

## Basecamp3.updateComment
Allows changing content of the message with an ID of `commentId` in the Basecamp with ID `basecampId`.

| Field        | Type  | Description
|--------------|-------|----------
| accountId    | String| Basecamp Account ID.
| accessToken  | String| OAuth2 Access Token from `getAccessToken` block.
| basecampId   | String| Basecamp ID.
| commentId    | String| Comment ID.
| content      | String| The body of the messag

## Basecamp3.getRecordings
Return a paginated list of records for the given type of recording.

| Field        | Type  | Description
|--------------|-------|----------
| accountId    | String| Basecamp Account ID.
| accessToken  | String| OAuth2 Access Token from `getAccessToken` block.
| type         | String| Must be `Comment`, `Document`, `Message`, `Question::Answer`, `Schedule::Entry`, `Todo`, `Todolist`, or `Upload`.
| bucket       | String| Single or comma separated list of Basecamp IDs. Default: All active Basecamps visible to the current user.
| status       | String| Options: `active`, `archived`, or `trashed`. Default: `active`
| sort         | String| Options: `created_at` or `updated_at`. Default: `created_at`.
| direction    | String| Options: `desc` or `asc`. Default: `desc`.

## Basecamp3.deleteRecording
mark the recording with an ID of `recordingId` in the Basecamp with ID `basecampId` as trashed.

| Field        | Type  | Description
|--------------|-------|----------
| accountId    | String| Basecamp Account ID.
| accessToken  | String| OAuth2 Access Token from `getAccessToken` block.
| basecampId   | String| Basecamp ID.
| recordingId  | String| Recording ID.

## Basecamp3.getDocuments
Returns a list of active documents in the Basecamp with an ID of `basecampId` and the vault with ID of `vaultId`.

| Field        | Type  | Description
|--------------|-------|----------
| accountId    | String| Basecamp Account ID.
| accessToken  | String| OAuth2 Access Token from `getAccessToken` block.
| basecampId   | String| Basecamp ID.
| vaultId      | String| Recording ID.

## Basecamp3.getSingleDocument
Return the document with an ID of `documentId` in the Basecamp with an ID of `basecampId`.

| Field        | Type  | Description
|--------------|-------|----------
| accountId    | String| Basecamp Account ID.
| accessToken  | String| OAuth2 Access Token from `getAccessToken` block.
| basecampId   | String| Basecamp ID.
| documentId   | String| Document ID.

## Basecamp3.createDocument
Publishes a document in the Basecamp with ID `basecampId` and under the vault with an ID of `vaultId`.

| Field        | Type  | Description
|--------------|-------|----------
| accountId    | String| Basecamp Account ID.
| accessToken  | String| OAuth2 Access Token from `getAccessToken` block.
| basecampId   | String| Basecamp ID.
| vaultId      | String| Recording ID.
| title        | String| Title of the document.
| content      | String| Body of the document.
| status       | String| Set to `active` to publish immediately.

## Basecamp3.updateSingleDocument
Allows changing the title and content of the document with an ID of `documentId` in the Basecamp with ID `basecampId`.

| Field        | Type  | Description
|--------------|-------|----------
| accountId    | String| Basecamp Account ID.
| accessToken  | String| OAuth2 Access Token from `getAccessToken` block.
| basecampId   | String| Basecamp ID.
| documentId   | String| Document ID.
| title        | String| Title of the document.
| content      | String| Body of the document.

## Basecamp3.getEvents
Returns a list of events for the recording with an ID of `recordingId` in the Basecamp with an ID of `basecampId`.

| Field        | Type  | Description
|--------------|-------|----------
| accountId    | String| Basecamp Account ID.
| accessToken  | String| OAuth2 Access Token from `getAccessToken` block.
| basecampId   | String| Basecamp ID.
| recordingId  | String| Recording ID.

## Basecamp3.getForwards
Returns a list of active forwards in the Basecamp with an ID of `basecampId` and the inbox with an ID of `inboxId`.

| Field        | Type  | Description
|--------------|-------|----------
| accountId    | String| Basecamp Account ID.
| accessToken  | String| OAuth2 Access Token from `getAccessToken` block.
| basecampId   | String| Basecamp ID
| inboxId      | String| Inbox ID.

## Basecamp3.getSingleForward
Returns the forward with an ID of `forwardId` in the Basecamp with an ID of `basecampId`.

| Field        | Type  | Description
|--------------|-------|----------
| accountId    | String| Basecamp Account ID.
| accessToken  | String| OAuth2 Access Token from `getAccessToken` block.
| basecampId   | String| Basecamp ID.
| forwardId    | String| Forward ID.

## Basecamp3.getInbox
Returns the inbox with an ID of `inboxId` for the Basecamp with an ID of `basecampId`.

| Field        | Type  | Description
|--------------|-------|----------
| accountId    | String| Basecamp Account ID.
| accessToken  | String| OAuth2 Access Token from `getAccessToken` block.
| basecampId   | String| Basecamp ID.
| inboxId      | String| Inbox ID.

## Basecamp3.getMessageBoard
Returns the message board for the Basecamp with an ID of `basecampId`.

| Field        | Type  | Description
|--------------|-------|----------
| accountId    | String| Basecamp Account ID.
| accessToken  | String| OAuth2 Access Token from `getAccessToken` block.
| basecampId   | String| Basecamp ID.
| boardId      | String| Board ID.

## Basecamp3.getMessages
Returns a list of active messages in the Basecamp with an ID of `basecampId` and the message board with ID of `boardId`.

| Field        | Type  | Description
|--------------|-------|----------
| accountId    | String| Basecamp Account ID.
| accessToken  | String| OAuth2 Access Token from `getAccessToken` block.
| basecampId   | String| Basecamp ID.
| boardId      | String| Board ID.

## Basecamp3.getSingleMessage
Returns the message with an ID of `messageId` in the Basecamp with an ID of `basecampId`.

| Field        | Type  | Description
|--------------|-------|----------
| accountId    | String| Basecamp Account ID.
| accessToken  | String| OAuth2 Access Token from `getAccessToken` block.
| basecampId   | String| Basecamp ID.
| messageId    | String| Message ID.

## Basecamp3.createMessage
Publishes a message in the Basecamp with ID `basecampId` and under the message board with an ID of `boardId`.

| Field        | Type  | Description
|--------------|-------|----------
| accountId    | String| Basecamp Account ID.
| accessToken  | String| OAuth2 Access Token from `getAccessToken` block.
| basecampId   | String| Basecamp ID.
| boardId      | String| Board ID.
| subject      | String| Title of the message.
| content      | String| Body of the message.

## Basecamp3.updateMessage
Allows changing the subject and content of the message with an ID of `messageId` in the Basecamp with ID `commentId`.

| Field        | Type  | Description
|--------------|-------|----------
| accountId    | String| Basecamp Account ID.
| accessToken  | String| OAuth2 Access Token from `getAccessToken` block.
| basecampId   | String| Basecamp ID.
| messageId    | String| Message ID.
| subject      | String| Title of the message.
| content      | String| Body of the message.

## Basecamp3.getAllPeople
Return all people visible to the current user.

| Field        | Type  | Description
|--------------|-------|----------
| accountId    | String| Basecamp Account ID.
| accessToken  | String| OAuth2 Access Token from `getAccessToken` block.

## Basecamp3.getPeopleOnBasecamp
Returns all active people on the Basecamp with the given ID.

| Field        | Type  | Description
|--------------|-------|----------
| accountId    | String| Basecamp Account ID.
| accessToken  | String| OAuth2 Access Token from `getAccessToken` block.
| basecampId   | String| 

## Basecamp3.createBasecampAccess
Allows granting new people access to a Basecamp.

| Field        | Type  | Description
|--------------|-------|----------
| accountId    | String| Basecamp Account ID.
| accessToken  | String| OAuth2 Access Token from `getAccessToken` block.
| basecampId   | String| Basecamp ID.
| people       | JSON  | An array of new people with name and email_address properties, and optional title and company_name properties. See README for more info.

## Basecamp3.grantBasecampAccess
Allows granting existing people access to a Basecamp.

| Field        | Type  | Description
|--------------|-------|----------
| accountId    | String| Basecamp Account ID.
| accessToken  | String| OAuth2 Access Token from `getAccessToken` block.
| basecampId   | String| Basecamp ID.
| people       | JSON  | An array of people IDs. See README for more info.

## Basecamp3.revokeBasecampAccess
Allows revoking access from existing people.

| Field        | Type  | Description
|--------------|-------|----------
| accountId    | String| Basecamp Account ID.
| accessToken  | String| OAuth2 Access Token from `getAccessToken` block.
| basecampId   | String| Basecamp ID.
| people       | JSON  | An array of people IDs. See README for more info.

## Basecamp3.getPingablePeople
Returns all people on this Basecamp account who can be pinged.

| Field        | Type  | Description
|--------------|-------|----------
| accountId    | String| Basecamp Account ID.
| accessToken  | String| OAuth2 Access Token from `getAccessToken` block.

## Basecamp3.getPerson
Returns the profile for the user with the given ID.

| Field        | Type  | Description
|--------------|-------|----------
| accountId    | String| Basecamp Account ID.
| accessToken  | String| OAuth2 Access Token from `getAccessToken` block.
| personId     | String| Person ID.

## Basecamp3.getMyInfo
Returns the current user's personal info.

| Field        | Type  | Description
|--------------|-------|----------
| accountId    | String| Basecamp Account ID.
| accessToken  | String| OAuth2 Access Token from `getAccessToken` block.

## Basecamp3.getQuestionAnswers
Returns a list of answers in the Basecamp with an ID of `basecampId` and the question with ID of `questionId`.

| Field        | Type  | Description
|--------------|-------|----------
| accountId    | String| Basecamp Account ID.
| accessToken  | String| OAuth2 Access Token from `getAccessToken` block.
| basecampId   | String| Basecamp ID.
| questionId   | String| Question ID.

## Basecamp3.getSingleQuestionAnswer
Returns the answer with an ID of `answerId` in the Basecamp with an ID of `basecampId`.

| Field        | Type  | Description
|--------------|-------|----------
| accountId    | String| Basecamp Account ID.
| accessToken  | String| OAuth2 Access Token from `getAccessToken` block.
| basecampId   | String| Basecamp ID.
| answerId     | String| Answer ID.

## Basecamp3.getQuestionnaire
Returns the questionnaire for the Basecamp with an ID of `questionnaireId`.

| Field              | Type  | Description
|--------------------|-------|----------
| accountId          | String| Basecamp Account ID.
| accessToken        | String| OAuth2 Access Token from `getAccessToken` block.
| basecampId         | String| Basecamp ID.
| questionnaireId    | String| Questionnaire id.

## Basecamp3.getQuestions
Return a list of questions in the Basecamp with an ID of `basecampId` and the questionnaire with ID of `questionnaireId`.

| Field              | Type  | Description
|--------------------|-------|----------
| accountId          | String| Basecamp Account ID.
| accessToken        | String| OAuth2 Access Token from `getAccessToken` block.
| basecampId         | String| Basecamp ID.
| questionnaireId    | String| Questionnaire ID.

## Basecamp3.getSingleQuestion
Return the question with an ID of `questionId` in the Basecamp with an ID of `basecampId`.

| Field        | Type  | Description
|--------------|-------|----------
| accountId    | String| Basecamp Account ID.
| accessToken  | String| OAuth2 Access Token from `getAccessToken` block.
| basecampId   | String| Basecamp ID.
| questionId   | String| Question ID.

## Basecamp3.getScheduleEntries
Return a paginated list of active schedule entries in the Basecamp with an ID of `basecampId` and the schedule with ID of `scheduleId`.

| Field        | Type  | Description
|--------------|-------|----------
| accountId    | String| Basecamp Account ID.
| accessToken  | String| OAuth2 Access Token from `getAccessToken` block.
| basecampId   | String| Basecamp ID.
| scheduleId   | String| Schedule ID.
| status       | String| When set to `archived` or `trashed`, will return archived or trashed schedule entries that are in this schedule.

## Basecamp3.getSingleScheduleEntry
Return the schedule entry with an ID of `entryId` in the Basecamp with an ID of `basecampId`.

| Field        | Type  | Description
|--------------|-------|----------
| accountId    | String| Basecamp Account ID.
| accessToken  | String| OAuth2 Access Token from `getAccessToken` block.
| basecampId   | String| Basecamp ID.
| entryId      | String| Schedule ID.

## Basecamp3.createScheduleEntry
Creates a schedule entry in the Basecamp with ID `basecampId` and under the schedule with an ID of `scheduleId`.

| Field         | Type  | Description
|---------------|-------|----------
| accountId     | String| Basecamp Account ID.
| accessToken   | String| OAuth2 Access Token from `getAccessToken` block.
| basecampId    | String| Basecamp ID.
| scheduleId    | String| Schedule ID.
| summary       | String| What this schedule entry is about
| startsAt      | Number| Timestamp for when this schedule entry begins
| endsAt        | Number| Timestamp for when this schedule entry ends
| description   | String| Containing more information about the schedule entry
| participantIds| String| An array of people IDs that will participate in this entry
| allDay        | String| When set to `true`, the schedule entry will not have a specific start or end time, and instead will be held for the entire day or days denoted in `starts_at` and `ends_at`
| notify        | String| When set to `true`, will notify the participants about the entry

## Basecamp3.updateScheduleEntry
Allows changing of the schedule entry with an ID of `entryId` in the Basecamp with ID `basecampId`.

| Field         | Type  | Description
|---------------|-------|----------
| accountId     | String| Basecamp Account ID.
| accessToken   | String| OAuth2 Access Token from `getAccessToken` block.
| basecampId    | String| Basecamp ID.
| entryId       | String| Schedule entry ID.
| summary       | String| What this schedule entry is about
| startsAt      | Number| Timestamp for when this schedule entry begins
| endsAt        | Number| Timestamp for when this schedule entry ends
| description   | String| Containing more information about the schedule entry
| participantIds| String| An array of people IDs that will participate in this entry
| allDay        | String| When set to `true`, the schedule entry will not have a specific start or end time, and instead will be held for the entire day or days denoted in `starts_at` and `ends_at`
| notify        | String| When set to `true`, will notify the participants about the entry

## Basecamp3.getSingleSchedule
Returns the schedule for the Basecamp with an ID of `basecampId`.

| Field        | Type  | Description
|--------------|-------|----------
| accountId    | String| Basecamp Account ID.
| accessToken  | String| OAuth2 Access Token from `getAccessToken` block.
| basecampId   | String| Basecamp ID.
| scheduleId   | String| Schedule ID.

## Basecamp3.getTemplates
Returns a list of active Templates visible to the current user sorted by most recently created Template first.

| Field        | Type  | Description
|--------------|-------|----------
| accountId    | String| Basecamp Account ID.
| accessToken  | String| OAuth2 Access Token from `getAccessToken` block.
| status       | String| When set to `archived` or `trashed`, will return archived or trashed Templates visible to the current user.

## Basecamp3.getSingleTemplate
Returns the Template with the given ID, granted they have access to it.

| Field        | Type  | Description
|--------------|-------|----------
| accountId    | String| Basecamp Account ID.
| accessToken  | String| OAuth2 Access Token from `getAccessToken` block.
| templateId   | String| templateId

## Basecamp3.createTemplate
Creates a new template.

| Field        | Type  | Description
|--------------|-------|----------
| accountId    | String| Basecamp Account ID.
| accessToken  | String| OAuth2 Access Token from `getAccessToken` block.
| name         | String| Name of template.
| description  | String| Description of template.

## Basecamp3.updateTemplate
Allows updating of a Template's `name` and `description`.

| Field        | Type  | Description
|--------------|-------|----------
| accountId    | String| Basecamp Account ID.
| accessToken  | String| OAuth2 Access Token from `getAccessToken` block.
| templateId   | String| Template ID.
| name         | String| New template name.
| description  | String| New template description.

## Basecamp3.deleteTemplate
Marks the Template with the given ID as trashed. Trashed Templates will be deleted from Basecamp 3 after 30 days.

| Field        | Type  | Description
|--------------|-------|----------
| accountId    | String| Basecamp Account ID.
| accessToken  | String| OAuth2 Access Token from `getAccessToken` block.
| templateId   | String| Template ID.

## Basecamp3.getProjectConstruction
Return the current state of the project construction.

| Field             | Type  | Description
|-------------------|-------|----------
| accountId         | String| Basecamp Account ID.
| accessToken       | String| OAuth2 Access Token from `getAccessToken` block.
| templateId        | String| Template ID.
| constructionId    | String| Project construction ID.

## Basecamp3.getToDoLists
Return a paginated list of active to-do lists in the Basecamp with an ID of `basecampId` and the to-do set with ID of `setId`.

| Field        | Type  | Description
|--------------|-------|----------
| accountId    | String| Basecamp Account ID.
| accessToken  | String| OAuth2 Access Token from `getAccessToken` block.
| basecampId   | String| Basecamp ID.
| setId        | String| Todo Set ID.

## Basecamp3.getSingleToDoList
Returns the to-do list with an ID of `listId` in the Basecamp with an ID of `basecampId`.

| Field        | Type  | Description
|--------------|-------|----------
| accountId    | String| Basecamp Account ID.
| accessToken  | String| OAuth2 Access Token from `getAccessToken` block.
| basecampId   | String| Basecamp ID.
| listId       | String| List ID.

## Basecamp3.createToDoList
Creates a to-do list in the Basecamp with ID `basecampId` and under the to-do set with an ID of `setId`.

| Field        | Type  | Description
|--------------|-------|----------
| accountId    | String| Basecamp Account ID.
| accessToken  | String| OAuth2 Access Token from `getAccessToken` block.
| basecampId   | String| Basecamp ID.
| setId        | String| To-do set ID.
| name         | String| Name of the to-do list.
| description  | String| Containing information about the to-do list.

## Basecamp3.updateToDoList
Allows changing the name and description of the to-do list with an ID of `listId` in the Basecamp with ID `basecampId`.

| Field        | Type  | Description
|--------------|-------|----------
| accountId    | String| Basecamp Account ID.
| accessToken  | String| OAuth2 Access Token from `getAccessToken` block.
| basecampId   | String| Basecamp ID.
| listId       | String| To-do list ID
| name         | String| Name of the to-do list.
| description  | String| Containing information about the to-do list.

## Basecamp3.getToDos
Returns a list of active to-dos in the Basecamp with an ID of `basecampId` and the to-do list with ID of `listId`.

| Field        | Type  | Description
|--------------|-------|----------
| accountId    | String| Basecamp Account ID.
| accessToken  | String| OAuth2 Access Token from `getAccessToken` block.
| basecampId   | String| Basecamp ID.
| listId       | String| List ID.
| status       | String| When set to `archived` or `trashed`, will return archived or trashed to-dos that are in this list.
| completed    | String| When set to true, will only return to-dos that are completed. Can be combined with the status parameter.

## Basecamp3.getSingleToDo
Return the to-do with an ID of `todoId` in the Basecamp with an ID of `basecampId`.

| Field        | Type  | Description
|--------------|-------|----------
| accountId    | String| Basecamp Account ID.
| accessToken  | String| OAuth2 Access Token from `getAccessToken` block.
| basecampId   | String| Basecamp ID.
| todoId       | String| To-do ID.

## Basecamp3.createToDo
Creates a to-do in the Basecamp with ID `basecampId` and under the to-do list with an ID of `listId`.

| Field        | Type  | Description
|--------------|-------|----------
| accountId    | String| Basecamp Account ID.
| accessToken  | String| OAuth2 Access Token from `getAccessToken` block.
| basecampId   | String| Basecamp ID.
| listId       | String| List ID.
| content      | String| What the to-do is for.
| description  | String| Containing information about the to-do.
| assigneeIds  | String| An array of people that will be assigned to this to-do.
| notify       | String| When set to `true`, will notify the assignees about being assigned.
| dueOn        | String| A `YYYY-mm-dd` date when the to-do should be completed.
| startsOn     | String| Allows the to-do to run from this date to the `dueOn` date.

## Basecamp3.updateToDo
Allows changing the to-do with an ID of `todoId` in the Basecamp with ID `basecampId`.

| Field        | Type  | Description
|--------------|-------|----------
| accountId    | String| Basecamp Account ID.
| accessToken  | String| OAuth2 Access Token from `getAccessToken` block.
| basecampId   | String| Basecamp ID.
| todoId       | String| To-do list ID.
| content      | String| What the to-do is for.
| description  | String| Containing information about the to-do.
| assigneeIds  | String| An array of people that will be assigned to this to-do.
| notify       | String| When set to `true`, will notify the assignees about being assigned.
| dueOn        | String| A `YYYY-mm-dd` date when the to-do should be completed.
| startsOn     | String| Allows the to-do to run from this date to the `dueOn` date.

## Basecamp3.completeToDo
Marks the to-do with an ID of `todoId` in the Basecamp with ID `basecampId` as completed.

| Field        | Type  | Description
|--------------|-------|----------
| accountId    | String| Basecamp Account ID.
| accessToken  | String| OAuth2 Access Token from `getAccessToken` block.
| basecampId   | String| Basecamp ID.
| todoId       | String| To-do ID.

## Basecamp3.uncompleteToDo
Marks the to-do with an ID of `todoId` in the Basecamp with ID `basecampId` as uncompleted.

| Field        | Type  | Description
|--------------|-------|----------
| accountId    | String| Basecamp Account ID.
| accessToken  | String| OAuth2 Access Token from `getAccessToken` block.
| basecampId   | String| Basecamp ID.
| todoId       | String| To-do ID.

## Basecamp3.repositionToDo
Allows changing the position of the to-do with an ID of `todoId` in the Basecamp with ID `basecampId`.

| Field        | Type  | Description
|--------------|-------|----------
| accountId    | String| Basecamp Account ID.
| accessToken  | String| OAuth2 Access Token from `getAccessToken` block.
| basecampId   | String| Basecamp ID.
| todoId       | String| Todo ID.
| position     | Number| Greater than or equal to one.

## Basecamp3.getToDoSet
Returns the to-do set for the Basecamp with an ID of `basecampId`.

| Field        | Type  | Description
|--------------|-------|----------
| accountId    | String| Basecamp Account ID.
| accessToken  | String| OAuth2 Access Token from `getAccessToken` block.
| basecampId   | String| Basecamp ID.
| setId        | String| To-do set ID.

## Basecamp3.getUploads
Returns a paginated list of active uploads in the Basecamp with an ID of `basecampId` and the vault with ID of `vaultId`.

| Field        | Type  | Description
|--------------|-------|----------
| accountId    | String| Basecamp Account ID.
| accessToken  | String| OAuth2 Access Token from `getAccessToken` block.
| basecampId   | String| Basecamp ID.
| vaultId      | String| Vault ID.

## Basecamp3.getSingleUpload
Returns the upload with an ID of `uploadId` in the Basecamp with an ID of `basecampId`.

| Field        | Type  | Description
|--------------|-------|----------
| accountId    | String| Basecamp Account ID.
| accessToken  | String| OAuth2 Access Token from `getAccessToken` block.
| basecampId   | String| Basecamp ID.
| uploadId     | String| Upload ID.

## Basecamp3.createUpload
Creates an upload in the Basecamp with ID `basecampId` and under the vault with an ID of `vaultId`.

| Field             | Type  | Description
|-------------------|-------|----------
| accountId         | String| Basecamp Account ID.
| accessToken       | String| OAuth2 Access Token from `getAccessToken` block.
| basecampId        | String| Basecamp ID.
| vaultId           | String| Vault ID.
| attachableSgid    | String| `attachable_sgid` for an uploaded attachment (from `createAttachment` method.)
| description       | String| Containing information about the upload.
| baseName          | String| An new file name for the upload.

## Basecamp3.updateUpload
Allows changing the `description` and `baseName` of the upload with an ID of `uploadId` in the Basecamp with ID `basecampId`.

| Field        | Type  | Description
|--------------|-------|----------
| accountId    | String| Basecamp Account ID.
| accessToken  | String| OAuth2 Access Token from `getAccessToken` block.
| basecampId   | String| Basecamp ID.
| uploadId     | String| Upload ID.
| description  | String| Containing information about the upload.
| baseName     | String| An new file name for the upload.

## Basecamp3.getVaults
Returns a list of vaults in the Basecamp with an ID of `basecampId` and the vault with ID of `vaultId`.

| Field        | Type  | Description
|--------------|-------|----------
| accountId    | String| Basecamp Account ID.
| accessToken  | String| OAuth2 Access Token from `getAccessToken` block.
| basecampId   | String| Basecamp ID.
| vaultId      | String| Vault ID.

## Basecamp3.getSingleVault
Returns the vault with an ID of `vaultId` in the Basecamp with an ID of `basecampId`.

| Field        | Type  | Description
|--------------|-------|----------
| accountId    | String| Basecamp Account ID.
| accessToken  | String| OAuth2 Access Token from `getAccessToken` block.
| basecampId   | String| 
| vaultId      | String| 

## Basecamp3.createVault
Creates a vault in the Basecamp with ID `basecampId` and under the vault with an ID of `vaultId`.

| Field        | Type  | Description
|--------------|-------|----------
| accountId    | String| Basecamp Account ID.
| accessToken  | String| OAuth2 Access Token from `getAccessToken` block.
| basecampId   | String| Basecamp ID.
| vaultId      | String| Vault ID.
| title        | String| Name of the vault.

## Basecamp3.updateVault
Allows changing the title of the vault with an ID of `vaultId` in the Basecamp with ID `basecampId`.

| Field        | Type  | Description
|--------------|-------|----------
| accountId    | String| Basecamp Account ID.
| accessToken  | String| OAuth2 Access Token from `getAccessToken` block.
| basecampId   | String| Basecamp ID.
| vaultId      | String| Vault ID.
| title        | String| New vault title.

## Basecamp3.getWebhooks
Returns all the webhooks from the basecamp with an ID of `basecampId`.

| Field        | Type  | Description
|--------------|-------|----------
| accountId    | String| Basecamp Account ID.
| accessToken  | String| OAuth2 Access Token from `getAccessToken` block.
| basecampId   | String| Basecamp ID.

## Basecamp3.getSingleWebhook
Returns the webhook with an ID of `webhookId` in the Basecamp with ID `basecampId`.

| Field        | Type  | Description
|--------------|-------|----------
| accountId    | String| Basecamp Account ID.
| accessToken  | String| OAuth2 Access Token from `getAccessToken` block.
| basecampId   | String| Basecamp ID.
| webhookId    | String| Webhook ID.

## Basecamp3.createWebhook
Creates a webhook in the Basecamp with ID `basecampId`.

| Field        | Type  | Description
|--------------|-------|----------
| accountId    | String| Basecamp Account ID.
| accessToken  | String| OAuth2 Access Token from `getAccessToken` block.
| basecampId   | String| 
| payloadUrl   | String| Payload url for the `HTTPS` url that Basecamp should call.
| types        | JSON  | An array of types, options given in the introduction.

## Basecamp3.updateWebhook
Allows changing the payload url and types of the webhook with an ID of `webhookId` in the Basecamp with ID `basecampId`.

| Field        | Type   | Description
|--------------|--------|----------
| accountId    | String | Basecamp Account ID.
| accessToken  | String | OAuth2 Access Token from `getAccessToken` block.
| basecampId   | String | Basecamp ID.
| webhookId    | String | Webhook ID.
| payloadUrl   | String | Payload url for the `HTTPS` url that Basecamp should call.
| types        | JSON   | An array of types, options given in the introduction.
| active       | Boolean| Boolean whether this webhook should be matching.

## Basecamp3.deleteWebhook
Deletes the webhook with an ID of `webhookId` in the Basecamp with ID `basecampId`.

| Field        | Type  | Description
|--------------|-------|----------
| accountId    | String| Basecamp Account ID.
| accessToken  | String| OAuth2 Access Token from `getAccessToken` block.
| basecampId   | String| Basecamp ID.
| webhookId    | String| Webhook ID.

## Basecamp3.getAccessToken
Returns `accessToken`.

| Field       | Type  | Description
|-------------|-------|----------
| clientId    | String| Basecamp integration Client ID.
| clientSecret| String| Basecamp integration Client Secret.
| redirectUri | String| Basecamp integration Redirect Uri.
| code        | String| OAuth2 code.

## Basecamp3.refreshAccessToken
Allows refresh accessToken.

| Field           | Type  | Description
|-----------------|-------|----------
| refreshToken    | String| OAuth2 Refresh Token from `getAccessToken` block.
| clientId        | String| Basecamp integration Client ID.
| clientSecret    | String| Basecamp integration Client Secret.
| redirectUri     | String| Basecamp integration Redirect Uri.

## Basecamp3.getAuthorization
Returns Authorization information.

| Field          | Type  | Description
|----------------|-------|----------
| accessToken    | String| OAuth2 Access Token from `getAccessToken` block.

