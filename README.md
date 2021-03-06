# CLI tool to verify valid email addresses

##### Follow below steps for this to work
1. Register for a free account at either/both [Never Bounce](https://neverbounce.com/) or [MailboxLayer](https://mailboxlayer.com/)

2. Create `apiKeys.js` file in root of project that

    A. Contains your credentials

    B. Exports your credentials according to below format

    ```
    module.exports = {
        neverbounce: {
            username: "1234567890",
            key: "abcdefghijklmnopqrstuv"
        },
        mailboxLayer: {
            key: "abcdefghijklmnopqrstuv"
        }
    };
    ```
3. Run `$ node check.js FILENAME SERVICECODE` and wait for the results **


** Things to consider
* SERVICECODE is `mbl` for Mailbox Layer or `nb` for Never Bounce
* FILENAME should be located in `/desktop` and include the .csv extension => `emailList.csv`
* The output will be written to `/desktop` as `FILENAME`+ `Results.csv` => `emailListResults.csv`
* To authenticate with NeverBounce, make sure you include your username and key in the `apiKeys.js` file. Run `$ node authenticate.js`
* Final Example: `$ node check.js emailList.csv mbl`