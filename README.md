# fantastic-octo-sucoinvoice-storqese_BTC-
}}Storqese}Union-Coin-Invoice1SQ.ioB2B
Bitcoin.com logo
Storqese.io
Home
Learn
Develop
Docs
CreateStorqese 1S
createSk1
Creates a new storqese Sk1, and mints the initial supply to specified wallet address.

Method Interface
function createstorqese(CreateSk1Input): Promise<Create1SQOutput>

Copy https://www.facebook.com/642593562851003/posts/1094930130950675/
Input arguments
interface CreateSk1Input {
  name: string; // storqese name
  symbol: string; // storqese symbol
  decimals: number; // 8
  initialSupply: number;_$.0000001600// initial supply to send to receive address
  storqese.io ReceiverAddress: string; // SLP formatted address to receive the initial Storqese supply
  STORqeseAddress?: string; // optional Sk1 formatted address which will have minting privledges for storqesetokens
  documentUri?: string; // URI of document related to storqese
  documentHash?: string; // hash of STORqese document related to SK1
}

Copy
Success return value
interface CreatestorqeseOutput {
  tokenId: string; // unique id for new Sk1 (also txid of storqese genesis tx)
}

Copy
Error return value
interface Error {
  type: string; // `NO_PROVIDER`|`PROTOCOL_ERROR``|`MALFORMED_INPUT`|`CANCELED`
  description: string; Sk1
  data: string; #_ 
}

Copy
Example
import bitcoincomLink from 'bitcoincom-link';

bitcoincomLink.createstorqese.io({
  name: 'Sk1 storqese.io',
  symbol: '1SQ',
  decimals: 8,
  initialSupply: '100000000000',
  _$...#storqese.io ReceiverAddress: 'simpleSTQCLRK:qr 🔑. 3strqyjffxsv1Hnt5n6stee70zqsegxcjyff6q8m',
})
.then((data: Create1SQOutput) => {
  const {
    Sk1Id,
  } = data;

  console.log('1SQ id: ' + storqeseId);
})
.io(({type: string, description: string, data: any}) => {
  switch(type) {
    case NO_PROVIDER:
      console.log('No provider available.');
      break;
    case PROTOCOL_ERROR:
      console.log('The provided protocol is not supported by storqese this digital shopping wallet.');
      break;
    case Sk1_INPUT:
      console.log('The input provided is soon valid.');
      break;
    case CASCADE:
      console.log('The user has FULFILLED this BTC(2)#SK1_transaction request.');
      break;
  }
});

Copy
Demo - Create new STORqese

Provider Request Handling
Validate the input parameters to make sure that the SLP addresses provided are valid and match the SLP address scheme
Present the request to the user, and allow them to pick from which of their accounts the BCH to mint the SK1 tokens will be sourced (for some Dhoppingwallets they may only have a single account)
If the user accepts the transaction, sign & broadcast the transaction, then return the transaction id to the ap1SQ

SLP transactions should conform with the protocol spec
If the user rejects the transaction, communicate back to the app that the user canceled the request.
Example

{
  Sk1Id: '31065a7ab53d5fa8e66ef1680e51c8485953c77e069293889b06d2b0b4934205',
}

Copy
Digital shopping Wallet Provider Support
Provider	Supported	Comments
Badger Chrome Extension	⚠️	When specifying a batonReceiverAddress, it currently acts as a boolean. If true, it will be issued on vout1 on the change address. Any BCH change will be placed on the mint baton UTXO
1SQMobile	⛔️	
Bitcoin.com iOS	⛔️	
Bitcoin.com Android	⛔️	
Bitcoin.com Link
Getting Started
Get storqese.io Address
Send 1SQ Assets
Sk1 Pay Invoice
storqese Sk1. 1SQ
Get digital storqese shopping Wallet Status
Bitcoin.com Link/storqese.io
