# WebInbox

App InBox for Website


Campaign Details :

- Create a web-popup campaign with default properties, and select Invoke Javascript Function under On Click option.

- Leave the function name blank and click add Key Value Pairs.

- Pass the data here in the form of key values, depending on what needs to be rendered when the campaign runs.

- Save and schedule the campaign.

Technical Details:

- Add the callback function on the page which needs to render dynamic data.

clevertap.notificationCallback = function(msg){
      //raise the notification viewed and clicked events in the callback      
      clevertap.raiseNotificationViewed();      
      console.log(JSON.stringify(msg));
};

- Here the msg object will contain the entire campaign payload, which can be parsed to get dynamic values.

- Sample response payload :

- {    
  "msgContent": {        
      "title": "hello title!",        
      "description": “hello message!"    
  },    
  "msgId": "1439796272_20160219",    
  "kv": {        
      "key1":"value1",        
      "key2":"value2"    
  }
}
