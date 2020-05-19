# Pin Message

Pinning a message allows administrators and owners of rooms to easily store messages which are important.

## Requirements

| Logged In | Permission | Setting |
| :--- | :--- | :--- |
| Yes | _none_ | `Message_AllowPinning` - "Allow Message Pinning" |

## Example Call

The only parameter that needs to be passed in is the [Message Object](../the-message-object.md) and as of release `0.46` you need to send the entire message object otherwise an internal error will happen \([fixed via pull request \#5087](https://github.com/RocketChat/Rocket.Chat/pull/5087)\).

```javascript
{
    "msg": "method",
    "method": "pinMessage",
    "id": "19",
    "params": [ fullMessageObject ]
}
```

## Example Response

The response of a message being pinned is a new chat message which contains the broadcast of the message pinning. See [Message Object Details](../the-message-object.md) for information about the response format.

```javascript
{
    "msg": "result",
    "id": "19",
    "result": {
        "t": "message_pinned",
        "rid": "QFtTnPJ4XbG634Skm",
        "ts": { "$date": 1480613343046 },
        "msg": "",
        "u": {
            "_id": "gHwBwDomPrCoQj7i2",
            "username": "bradley"
        },
        "groupable": false,
        "attachments": [{
            "text": "test",
            "author_name": "bradley",
            "author_icon": "/avatar/bradley.jpg?_dc=0",
            "ts": { "$date": 1480613302330 }
        }],
        "_updatedAt": { "$date": 1480613343046 },
        "_id": "sBYLyaHFkMdr7LKGt"
    }
}
```

## See Also

* [The Message Object](../the-message-object.md)
* [Pinning Messages User Guide](../../../user-guides/messaging.md)

