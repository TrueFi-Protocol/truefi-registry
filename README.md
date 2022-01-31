# TrueFi Registry

<br/>
<center><img src='https://raw.githubusercontent.com/trusttoken/truefi-registry/main/truefi.svg' height="200"></center>
<br/>

The TrueFi registry contains public metadata for TrueFi users and participants.

The [TrueFi](https://app.truefi.io) platform utilizes assets from this repository to display detailed information associated with specific entities.

<br/>

## How to add profile data

Profile metadata will be read from a json file corresponding to an entity's active wallet address.

First of all change the branch to "staging" on the left side. 

Create a new directory under the correct network <b>profiles/mainnet</b> or <b>profiles/ropsten</b>.

The directory name should be the entity's wallet address used to participate on TrueFi and should contain the entity's profile data in a file titled <b>profile.json</b> with an optional logo file <b>logo.svg</b>.

Profile data should follow the following structure:

<br/>

```
{
  "name": "Invictus Capital",
  "address": "0xCAFD96A3475aa9afcC66bc5f9FF589C74ce6A4Bc",
  "website": "https://invictuscapital.com/en/",
  "description": "Invictus Capital offers alternative investment products for the modern investor. They believe investing should be convenient, transparent and low-cost.",
  "logoURI": "",
  "explorer": "https://etherscan.io/address/0xCAFD96A3475aa9afcC66bc5f9FF589C74ce6A4Bc/",
  "status": "active",
  "github": "",
  "forumPost": "https://forum.truefi.io/t/invictus-capital-borrow-request/82",
  "socials": {
    "twitter" : {
      "url": "https://twitter.com/ic_invictus",
      "handle": ""
    },
    "linkedin": {
      "url": "https://www.linkedin.com/company/invictuscapital/",
      "handle": ""
    }
  }
}
```
<br/>

Of these fields <b>name and address are required.</b>

If an optional field is not to be included leave it blank with an empty string `""`.

For social links, all supported platforms are listed above.
Each platform is optional, if any are not to be included simply delete them from the list -
if no social platforms are to be included enter an empty object for the socials field `{}`

<br/>

### Adding profiles to the index

Once the profile data has been completed, the entity's address will need to be added to the index.

For mainnet addresses append the address and entity name to <b>profiles/mainnet/index.json</b>
the key should be the address and name the value ex.

```
{
  ...
  "0x83C1B27276108c0F68c52c2319beEd4646061A1F": "TrustToken Test",
  "0x0n3WAddR3ss00000000000000000000000000000": "New Entity"
}
```

<br/><br/>
