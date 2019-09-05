# ojet-7-expense-tracker-ws
Web Services for Expense Tracker App


### Provide Mock Data via the JSON Server
In this part, you set up the JSON Server to publish mock data that will be visualized in the Oracle JET application that you'll create via the instructions that follow.

1. Set up the JSON Server, as follows:
npm install -g json-server
Details: https://github.com/typicode/json-server

2. Run in the Terminal window:
json-server --watch employeeData.json
Go to http://localhost:3000/employees and see your data via your fake REST endpoint:


### Workflow
```bash
# Install
npm install

# Run Expense Server (On Port 5000)
npm run expense-server

# Run OAuth Server (On Port 9000)
npm run oauth-server

# Run Expense Server with OAuth Secutiry Enabled
npm run expense-server-with-oauth

```

### OAuth Usage
```bash
# Registering a user
# POST with application/x-www-form-urlencoded encoding
POST to http://localhost:9000/register with {"username":"tom", "password":"jerry"}

# Log In
# POST with application/x-www-form-urlencoded encoding
# grant_type=password, client_id & client_secret can be random strings
POST to http://localhost:9000/login with username, password, grant_type, client_id, client_secret

# Verify token
# Ex: Authorization: Bearer d105b24fce14e48e6466aeab4be7378d86b6359f
GET to http://localhost:9000/check with access token in header
curl -H "Authorization: Bearer $ACCESS_TOKEN" http://localhost:9000/check
```

### References
- [Blog on Creation Node OAuth 2 Server](https://blog.cloudboost.io/how-to-make-an-oauth-2-server-with-node-js-a6db02dc2ce7)
- [Reference Implementation](https://github.com/Meeks91/nodeJS_OAuth2Example)
