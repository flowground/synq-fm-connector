# ![LOGO](logo.png) SYNQ Video **flow**ground Connector

## Description

A generated **flow**ground connector for the SYNQ Video API (version 1.9.1).

Generated from: https://api.apis.guru/v2/specs/synq.fm/1.9.1/swagger.json<br/>
Generated at: 2019-05-07T17:44:20+03:00

## API Description

* [Sign up for a developer API key!](https://www.synq.fm/register)
* [SYNQ API Guide](/)

## Authorization

This API does not require authorization.

## Actions

### Create a new video, optionally setting some metadata fields.

> Create a new video, optionally setting some metadata fields. You may optionally set some of the metadata associated with the video. Only fields inside the "userdata" field can be set.

*Tags:* `video`

### Return details about a video.

> Return details about a video. You may optionally request that only some of the metadata fields are returned.

*Tags:* `video`

### Perform a JavaScript query to return video objects matching any desired criteria.

> Find videos matching any criteria, by running a JavaScript function over each video object. A detailed tutorial on how to use this functionality is available on the [documentation page](https://www.synq.fm/queries-video-api/).

*Tags:* `video`

### Returns urls for streaming.

> Returns a stream url that you can stream to from your broadcasting software, and a playback url people can use to watch the stream.

*Tags:* `video`

### Update a video's metadata.

> Update a video's metadata through JavaScript code. Only fields inside the "userdata" object can be set.

*Tags:* `video`

### Return parameters needed for uploading a video file.

> Return parameters needed for uploading a video file to Amazon Simple Storage Service. See http://docs.aws.amazon.com/AmazonS3/latest/API/sigv4-post-example.html as well as the language-specific code-examples.<br/>
> #### *Example request*<br/>
> ```shell<br/>
> curl -s https://api.synq.fm/v1/video/upload \<br/>
>   -F api_key=${SYNQ_API_KEY} \<br/>
>   -F video_id=2d81c30ce62f4dfdb501dbca96c7ae56<br/>
> ```<br/>
> <br/>
> #### *Example response*<br/>
> ```json<br/>
> {<br/>
>   "action": "https://synqfm.s3.amazonaws.com/",<br/>
>   "AWSAccessKeyId": "AKIAIP77Y7MMX3ITZMFA",<br/>
>   "Content-Type": "video/mp4",<br/>
>   "Policy": "eyJleHBpcmF0aW9uIiA6ICIyMDE2LTA0LTIyVDE5OjAyOjI2LjE3MloiLCAiY29uZGl0aW9ucyIgOiBbeyJidWNrZXQiIDogInN5bnFmbSJ9LCB7ImFjbCIgOiAicHVibGljLXJlYWQifSwgWyJzdGFydHMtd2l0aCIsICIka2V5IiwgInByb2plY3RzLzZlLzYzLzZlNjNiNzUyYTE4NTRkZGU4ODViNWNjNDcyZWRmNTY5L3VwbG9hZHMvdmlkZW9zLzJkLzgxLzJkODFjMzBjZTYyZjRkZmRiNTAxZGJjYTk2YzdhZTU2Lm1wNCJdLCBbInN0YXJ0cy13aXRoIiwgIiRDb250ZW50LVR5cGUiLCAidmlkZW8vbXA0Il0sIFsiY29udGVudC1sZW5ndGgtcmFuZ2UiLCAwLCAxMDk5NTExNjI3Nzc2XV19",<br/>
>   "Signature": "ysqDemlKXKr6hKzVFP0hCGgf/cs=",<br/>
>   "acl": "public-read",<br/>
>   "key": "projects/6e/63/6e63b752a1854dde885b5cc472edf569/uploads/videos/2d/81/2d81c30ce62f4dfdb501dbca96c7ae56.mp4"<br/>
> }<br/>
> ```<br/>
> <br/>
> To upload the file, you can then make a multipart POST request to the URL in `action`, and for all the other parameters returned, set them as form parameters.<br/>
> <br/>
> Given the parameters above, you would upload a file `test.mp4` using cURL like this:<br/>
> <br/>
> ```shell<br/>
> curl -s https://synqfm.s3.amazonaws.com/ \<br/>
>   -F AWSAccessKeyId="AKIAIP77Y7MMX3ITZMFA" \<br/>
>   -F Content-Type="video/mp4" \<br/>
>   -F Policy="eyJleHBpcmF0aW9uIiA6ICIyMDE2LTA0LTIyVDE5OjAyOjI2LjE3MloiLCAiY29uZGl0aW9ucyIgOiBbeyJidWNrZXQiIDogInN5bnFmbSJ9LCB7ImFjbCIgOiAicHVibGljLXJlYWQifSwgWyJzdGFydHMtd2l0aCIsICIka2V5IiwgInByb2plY3RzLzZlLzYzLzZlNjNiNzUyYTE4NTRkZGU4ODViNWNjNDcyZWRmNTY5L3VwbG9hZHMvdmlkZW9zLzJkLzgxLzJkODFjMzBjZTYyZjRkZmRiNTAxZGJjYTk2YzdhZTU2Lm1wNCJdLCBbInN0YXJ0cy13aXRoIiwgIiRDb250ZW50LVR5cGUiLCAidmlkZW8vbXA0Il0sIFsiY29udGVudC1sZW5ndGgtcmFuZ2UiLCAwLCAxMDk5NTExNjI3Nzc2XV19" \<br/>
>   -F Signature="ysqDemlKXKr6hKzVFP0hCGgf/cs=" \<br/>
>   -F acl="public-read" \<br/>
>   -F key="projects/6e/63/6e63b752a1854dde885b5cc472edf569/uploads/videos/2d/81/2d81c30ce62f4dfdb501dbca96c7ae56.mp4" \<br/>
>   -F file="@my_video_file.mp4"<br/>
> ```

*Tags:* `video`

### Return embeddable url to an uploader widget

> Returns an embeddable url, that contains an uploader widget that allows you to easily upload any mp4. Great way to simplify the uploading process for end users.

*Tags:* `video`

## License

**flow**ground :- Telekom iPaaS / synq-fm-connector<br/>
Copyright © 2019, [Deutsche Telekom AG](https://www.telekom.de)<br/>
contact: flowground@telekom.de

All files of this connector are licensed under the Apache 2.0 License. For details
see the file LICENSE on the toplevel directory.
