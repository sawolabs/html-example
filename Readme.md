# SAWO HTML 
The HyperText Markup Language or HTML is the standard markup language for documents designed to be displayed in a web browser.
# Let's Get your HTML running with SAWO 

## Steps
1.To use SAWO Login you would need an API key which can be obtained by creating a project in the [sawo dashboard](https://dev.sawolabs.com/)

2.Once you create your project, you would need to set your project name and hostname.

3.Copy the API key from the project and keep it safe and secure.

4.On your source, create a container for sawo component inside body tag
```
<div id="sawo-container" style="height: 300px; width: 300px;"></div>
``` 

5.Add the snippet at bottom of source inside body tag
```
<script src="https://websdk.sawolabs.com/sawo.min.js"></script>    
<script>
    var config = {
        // should be same as the id of the container created on 3rd step
        containerID: "sawo-container",
        // can be one of 'email' or 'phone_number_sms'
        identifierType: "phone_number_sms",
        // Add the API key copied from 2nd step
        apiKey: "",
        // Add a callback here to handle the payload sent by sdk
        onSuccess: (payload) => {
            console.log(payload)
        },
    };
    var sawo = new Sawo(config);
    sawo.showForm();
</script>
```
6.Once the SAWO SDK is successfully set up, a login form will be rendered in the provided container

# It's okay, we get it! You got Stuck!😞 Feel free to contact us on #ask-for-help on our [Discord](https://discord.com/invite/TpnCfMUE5P)
