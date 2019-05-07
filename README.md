# ![LOGO](logo.png) Content Moderator Client **flow**ground Connector

## Description

A generated **flow**ground connector for the Content Moderator Client API (version 1.0).

Generated from: https://api.apis.guru/v2/specs/azure.com/cognitiveservices-ContentModerator/1.0/swagger.json<br/>
Generated at: 2019-05-07T17:37:43+03:00

## API Description

You use the API to scan your content as it is generated. Content Moderator then processes your content and sends the results along with relevant information either back to your systems or to the built-in review tool. You can use this information to take decisions e.g. take it down, send to human judge, etc.

When using the API, images need to have a minimum of 128 pixels and a maximum file size of 4MB. 
Text can be at most 1024 characters long. 
If the content passed to the text API or the image API exceeds the size limits, the API will return an error code that informs about the issue.

## Authorization

Supported authorization schemes:
- API Key
## Actions

### Gets all the Image Lists.

*Tags:* `ListManagementImageLists`

### Creates an image list.

*Tags:* `ListManagementImageLists`

#### Input Parameters
* `Content-Type` - _required_ - The content type.

### Deletes image list with the list Id equal to list Id passed.

*Tags:* `ListManagementImageLists`

#### Input Parameters
* `listId` - _required_ - List Id of the image list.

### Returns the details of the image list with list Id equal to list Id passed.

*Tags:* `ListManagementImageLists`

#### Input Parameters
* `listId` - _required_ - List Id of the image list.

### Updates an image list with list Id equal to list Id passed.

*Tags:* `ListManagementImageLists`

#### Input Parameters
* `listId` - _required_ - List Id of the image list.
* `Content-Type` - _required_ - The content type.

### Refreshes the index of the list with list Id equal to list Id passed.

*Tags:* `ListManagementImageLists`

#### Input Parameters
* `listId` - _required_ - List Id of the image list.

### Deletes all images from the list with list Id equal to list Id passed.

*Tags:* `ListManagementImage`

#### Input Parameters
* `listId` - _required_ - List Id of the image list.

### Gets all image Ids from the list with list Id equal to list Id passed.

*Tags:* `ListManagementImage`

#### Input Parameters
* `listId` - _required_ - List Id of the image list.

### Add an image to the list with list Id equal to list Id passed.

*Tags:* `ListManagementImage`

#### Input Parameters
* `listId` - _required_ - List Id of the image list.
* `tag` - _optional_ - Tag for the image.
* `label` - _optional_ - The image label.

### Deletes an image from the list with list Id and image Id passed.

*Tags:* `ListManagementImage`

#### Input Parameters
* `listId` - _required_ - List Id of the image list.
* `ImageId` - _required_ - Id of the image.

### gets all the Term Lists

*Tags:* `ListManagementTermLists`

### Creates a Term List

*Tags:* `ListManagementTermLists`

#### Input Parameters
* `Content-Type` - _required_ - The content type.

### Deletes term list with the list Id equal to list Id passed.

*Tags:* `ListManagementTermLists`

#### Input Parameters
* `listId` - _required_ - List Id of the image list.

### Returns list Id details of the term list with list Id equal to list Id passed.

*Tags:* `ListManagementTermLists`

#### Input Parameters
* `listId` - _required_ - List Id of the image list.

### Updates an Term List.

*Tags:* `ListManagementTermLists`

#### Input Parameters
* `listId` - _required_ - List Id of the image list.
* `Content-Type` - _required_ - The content type.

### Refreshes the index of the list with list Id equal to list ID passed.

*Tags:* `ListManagementTermLists`

#### Input Parameters
* `listId` - _required_ - List Id of the image list.
* `language` - _required_ - Language of the terms.

### Deletes all terms from the list with list Id equal to the list Id passed.

*Tags:* `ListManagementTerm`

#### Input Parameters
* `listId` - _required_ - List Id of the image list.
* `language` - _required_ - Language of the terms.

### Gets all terms from the list with list Id equal to the list Id passed.

*Tags:* `ListManagementTerm`

#### Input Parameters
* `listId` - _required_ - List Id of the image list.
* `language` - _required_ - Language of the terms.
* `offset` - _optional_ - The pagination start index.
* `limit` - _optional_ - The max limit.

### Deletes a term from the list with list Id equal to the list Id passed.

*Tags:* `ListManagementTerm`

#### Input Parameters
* `listId` - _required_ - List Id of the image list.
* `term` - _required_ - Term to be deleted
* `language` - _required_ - Language of the terms.

### Add a term to the term list with list Id equal to list Id passed.

*Tags:* `ListManagementTerm`

#### Input Parameters
* `listId` - _required_ - List Id of the image list.
* `term` - _required_ - Term to be deleted
* `language` - _required_ - Language of the terms.

### Returns probabilities of the image containing racy or adult content.

*Tags:* `ImageModeration`

#### Input Parameters
* `CacheImage` - _optional_ - Whether to retain the submitted image for future use; defaults to false if omitted.

### Returns the list of faces found.

*Tags:* `ImageModeration`

#### Input Parameters
* `CacheImage` - _optional_ - Whether to retain the submitted image for future use; defaults to false if omitted.

### Fuzzily match an image against one of your custom Image Lists. You can create and manage your custom image lists using <a href="/docs/services/578ff44d2703741568569ab9/operations/578ff7b12703741568569abe">this</a> API. <br/>
> <br/>
> Returns ID and tags of matching image.<br/><br/>
> <br/><br/>
> Note: Refresh Index must be run on the corresponding Image List before additions and removals are reflected in the response.

*Tags:* `ImageModeration`

#### Input Parameters
* `listId` - _optional_ - The list Id.
* `CacheImage` - _optional_ - Whether to retain the submitted image for future use; defaults to false if omitted.

### Returns any text found in the image for the language specified. If no language is specified in input then the detection defaults to English.

*Tags:* `ImageModeration`

#### Input Parameters
* `language` - _required_ - Language of the terms.
* `CacheImage` - _optional_ - Whether to retain the submitted image for future use; defaults to false if omitted.
* `enhanced` - _optional_ - When set to True, the image goes through additional processing to come with additional candidates.

image/tiff is not supported when enhanced is set to true

Note: This impacts the response time.

### This operation will detect the language of given input content. Returns the <a href="http://www-01.sil.org/iso639-3/codes.asp">ISO 639-3 code</a> for the predominant language comprising the submitted text. Over 110 languages supported.

*Tags:* `TextModeration`

#### Input Parameters
* `Content-Type` - _required_ - The content type.
    Possible values: text/plain, text/html, text/xml, text/markdown.

### Detect profanity and match against custom and shared blacklists

> Detects profanity in more than 100 languages and match against custom and shared blacklists.

*Tags:* `TextModeration`

#### Input Parameters
* `language` - _optional_ - Language of the text.
* `autocorrect` - _optional_ - Autocorrect text.
* `PII` - _optional_ - Detect personal identifiable information.
* `listId` - _optional_ - The list Id.
* `classify` - _optional_ - Classify input.
* `Content-Type` - _required_ - The content type.
    Possible values: text/plain, text/html, text/xml, text/markdown.

### A job Id will be returned for the content posted on this endpoint. <br/>
> <br/>
> Once the content is evaluated against the Workflow provided the review will be created or ignored based on the workflow expression.<br/>
> <br/>
> <h3>CallBack Schemas </h3><br/>
> <br/>
> <p><br/>
> <h4>Job Completion CallBack Sample</h4><br/><br/>
> <br/>
> {<br/><br/>
>   "JobId": "<Job Id>,<br/><br/>
>   "ReviewId": "<Review Id, if the Job resulted in a Review to be created>",<br/><br/>
>   "WorkFlowId": "default",<br/><br/>
>   "Status": "<This will be one of Complete, InProgress, Error>",<br/><br/>
>   "ContentType": "Image",<br/><br/>
>   "ContentId": "<This is the ContentId that was specified on input>",<br/><br/>
>   "CallBackType": "Job",<br/><br/>
>   "Metadata": {<br/><br/>
>     "adultscore": "0.xxx",<br/><br/>
>     "a": "False",<br/><br/>
>     "racyscore": "0.xxx",<br/><br/>
>     "r": "True"<br/><br/>
>   }<br/><br/>
> }<br/><br/>
> <br/>
> </p><br/>
> <p><br/>
> <h4>Review Completion CallBack Sample</h4><br/><br/>
> <br/>
> {<br/>
>   "ReviewId": "<Review Id>",<br/><br/>
>   "ModifiedOn": "2016-10-11T22:36:32.9934851Z",<br/><br/>
>   "ModifiedBy": "<Name of the Reviewer>",<br/><br/>
>   "CallBackType": "Review",<br/><br/>
>   "ContentId": "<The ContentId that was specified input>",<br/><br/>
>   "Metadata": {<br/><br/>
>     "adultscore": "0.xxx",<br/>
>     "a": "False",<br/><br/>
>     "racyscore": "0.xxx",<br/><br/>
>     "r": "True"<br/><br/>
>   },<br/><br/>
>   "ReviewerResultTags": {<br/><br/>
>     "a": "False",<br/><br/>
>     "r": "True"<br/><br/>
>   }<br/><br/>
> }<br/><br/>
> <br/>
> </p>.

*Tags:* `Reviews`

#### Input Parameters
* `teamName` - _required_ - Your team name.
* `ContentType` - _required_ - Image, Text or Video.
    Possible values: Image, Text, Video.
* `ContentId` - _required_ - Id/Name to identify the content submitted.
* `WorkflowName` - _required_ - Workflow Name that you want to invoke.
* `CallBackEndpoint` - _optional_ - Callback endpoint for posting the create job result.
* `Content-Type` - _required_ - The content type.
    Possible values: application/json, image/jpeg.

### Get the Job Details for a Job Id.

*Tags:* `Reviews`

#### Input Parameters
* `teamName` - _required_ - Your Team Name.
* `JobId` - _required_ - Id of the job.

### The reviews created would show up for Reviewers on your team. As Reviewers complete reviewing, results of the Review would be POSTED (i.e. HTTP POST) on the specified CallBackEndpoint.<br/>
> <br/>
> <h3>CallBack Schemas </h3><br/>
> <h4>Review Completion CallBack Sample</h4><br/>
> <p><br/>
> {<br/><br/>
>   "ReviewId": "<Review Id>",<br/><br/>
>   "ModifiedOn": "2016-10-11T22:36:32.9934851Z",<br/><br/>
>   "ModifiedBy": "<Name of the Reviewer>",<br/><br/>
>   "CallBackType": "Review",<br/><br/>
>   "ContentId": "<The ContentId that was specified input>",<br/><br/>
>   "Metadata": {<br/><br/>
>     "adultscore": "0.xxx",<br/><br/>
>     "a": "False",<br/><br/>
>     "racyscore": "0.xxx",<br/><br/>
>     "r": "True"<br/><br/>
>   },<br/><br/>
>   "ReviewerResultTags": {<br/><br/>
>     "a": "False",<br/><br/>
>     "r": "True"<br/><br/>
>   }<br/><br/>
> }<br/><br/>
> <br/>
> </p>.

*Tags:* `Reviews`

#### Input Parameters
* `UrlContentType` - _required_ - The content type.
* `teamName` - _required_ - Your team name.
* `subTeam` - _optional_ - SubTeam of your team, you want to assign the created review to.

### Returns review details for the review Id passed.

*Tags:* `Reviews`

#### Input Parameters
* `teamName` - _required_ - Your Team Name.
* `reviewId` - _required_ - Id of the review.

### The reviews created would show up for Reviewers on your team. As Reviewers complete reviewing, results of the Review would be POSTED (i.e. HTTP POST) on the specified CallBackEndpoint.<br/>
> <br/>
> <h3>CallBack Schemas </h3><br/>
> <h4>Review Completion CallBack Sample</h4><br/>
> <p><br/>
> {<br/><br/>
>   "ReviewId": "<Review Id>",<br/><br/>
>   "ModifiedOn": "2016-10-11T22:36:32.9934851Z",<br/><br/>
>   "ModifiedBy": "<Name of the Reviewer>",<br/><br/>
>   "CallBackType": "Review",<br/><br/>
>   "ContentId": "<The ContentId that was specified input>",<br/><br/>
>   "Metadata": {<br/><br/>
>     "adultscore": "0.xxx",<br/><br/>
>     "a": "False",<br/><br/>
>     "racyscore": "0.xxx",<br/><br/>
>     "r": "True"<br/><br/>
>   },<br/><br/>
>   "ReviewerResultTags": {<br/><br/>
>     "a": "False",<br/><br/>
>     "r": "True"<br/><br/>
>   }<br/><br/>
> }<br/><br/>
> <br/>
> </p>.

*Tags:* `Reviews`

#### Input Parameters
* `teamName` - _required_ - Your team name.
* `reviewId` - _required_ - Id of the review.
* `startSeed` - _optional_ - Time stamp of the frame from where you want to start fetching the frames.
* `noOfRecords` - _optional_ - Number of frames to fetch.
* `filter` - _optional_ - Get frames filtered by tags.

### The reviews created would show up for Reviewers on your team. As Reviewers complete reviewing, results of the Review would be POSTED (i.e. HTTP POST) on the specified CallBackEndpoint.<br/>
> <br/>
> <h3>CallBack Schemas </h3><br/>
> <h4>Review Completion CallBack Sample</h4><br/>
> <p><br/>
> {<br/><br/>
>   "ReviewId": "<Review Id>",<br/><br/>
>   "ModifiedOn": "2016-10-11T22:36:32.9934851Z",<br/><br/>
>   "ModifiedBy": "<Name of the Reviewer>",<br/><br/>
>   "CallBackType": "Review",<br/><br/>
>   "ContentId": "<The ContentId that was specified input>",<br/><br/>
>   "Metadata": {<br/><br/>
>     "adultscore": "0.xxx",<br/><br/>
>     "a": "False",<br/><br/>
>     "racyscore": "0.xxx",<br/><br/>
>     "r": "True"<br/><br/>
>   },<br/><br/>
>   "ReviewerResultTags": {<br/><br/>
>     "a": "False",<br/><br/>
>     "r": "True"<br/><br/>
>   }<br/><br/>
> }<br/><br/>
> <br/>
> </p>.

*Tags:* `Reviews`

#### Input Parameters
* `teamName` - _required_ - Your team name.
* `reviewId` - _required_ - Id of the review.
* `timescale` - _optional_ - Timescale of the video you are adding frames to.

### Publish video review to make it available for review.

*Tags:* `Reviews`

#### Input Parameters
* `teamName` - _required_ - Your team name.
* `reviewId` - _required_ - Id of the review.

### This API adds a transcript file (text version of all the words spoken in a video) to a video review. The file should be a valid WebVTT format.

*Tags:* `Reviews`

#### Input Parameters
* `teamName` - _required_ - Your team name.
* `reviewId` - _required_ - Id of the review.
* `Content-Type` - _required_ - The content type.
    Possible values: text/plain.

### This API adds a transcript screen text result file for a video review. Transcript screen text result file is a result of Screen Text API . In order to generate transcript screen text result file , a transcript file has to be screened for profanity using Screen Text API.

*Tags:* `Reviews`

#### Input Parameters
* `Content-Type` - _required_ - The content type.
* `teamName` - _required_ - Your team name.
* `reviewId` - _required_ - Id of the review.

## License

**flow**ground :- Telekom iPaaS / azure-com-cognitiveservices-content-moderator-connector<br/>
Copyright © 2019, [Deutsche Telekom AG](https://www.telekom.de)<br/>
contact: flowground@telekom.de

All files of this connector are licensed under the Apache 2.0 License. For details
see the file LICENSE on the toplevel directory.
