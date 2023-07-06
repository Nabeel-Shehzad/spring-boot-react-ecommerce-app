Set the environmental variables which will be impacted on docker-compose.yml.
   
    1. Rename the file ".env-sample" to ".env".     
    2. (Optional Step) You need to create a Stripe account and Google OAuth credentials.
       The application works even if you don't create this account, only the payment and OAuth functionality will not work.
       These accounts doesn't charge you anything and are absolutely free.<br/><br/>

       You need to set below two env variables.<br/><br/>

       REACT_APP_STRIPE_PUBLISH_KEY=<Your Stripe Publishable Key>

       Go [Here](https://dashboard.stripe.com/register) to create a Stripe account.
       <br/><br/>
       REACT_APP_GOOGLE_AUTH_CLIENT_ID=<Your Google AUTH Client ID>

       Go [Here](https://console.developers.google.com) to create Google OAuth Credentials.

3. Build all the microservices and run the app using docker-compose. This is done using ./start-all.sh script which creates the network and set the container dependencies based on the config mention in the docker-compose.yml. 
   This will build all the jar files and run all the services.
   ```
      ./start-all.sh
   ```

4. If you are making any change in the code then you need to you ./stop-all.sh to clean up the jars created by ./start-all.sh script.