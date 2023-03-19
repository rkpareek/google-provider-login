# google-provider-login
    Automate 'login with google' yes is not so easy,
    google have more secure and dynamic DOM login popup-interface.
    Google is now two kind of popup inteface and both are completely different.
    This package lets you the flexibility to logs you into your website through
    both the login interface.
    This package works only with nightwatch.js to login with google provider.
    Install the package and get into your project:
    require('google-provider-login')
Use:
     var googleLogin = require('google-provider-login')

     @test
     client
        .click() //click on google provider,
        // Call googleLogin only after provider window open.
        .perform(function(client, done){
            googleLogin(client, googleEmail, googlePass, function(res){
            // a callback function

                // If login was successful it will return true otherwise false

                console.log(res)   //true/false

                /*
                 Your code based on callback response**
                 */

            })
        });
        .done(end);
