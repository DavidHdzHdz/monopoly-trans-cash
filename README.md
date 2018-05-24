# \<monopoly-trans-cash\>

**Install the Polymer-CLI**
```
$ npm install polymer-cli
```
**Viewing Your Element**
```
$ polymer serve
```
**Running Tests**
```
$ polymer test
```

### Description:
This element received two json like this:

* first on property 'to':
like this:
```json
[
  {
    "id" : "PABCDEF002",
    "alias" : "userDefault1",
    "amount" : 10000,
    "status" : "playing"
  },
  {
    "id" : "PABCDEF003",
    "alias" : "userDefault2",
    "amount" : 10000,
    "status" : "playing"
  }
]
```
if we named this json users the tag will be:
**<monopoly-trans-cash to="{{users}}">**

* second parameter is from that received a json like this:

```json
  {
    "id" : "PABCDEF001",
    "alias" : "loggedUser",
    "amount" : 10000,
    "status" : "playing"
  }
```
then if we named loggedUser to json the tag with parameters must be like this:
**<monopoly-trans-cash to="{{users}}" from="{{loggedUser}}">**

### For receive detail of doTransactio

we must to select component with and listen the 'cash-transaction' event
```javascript
const element = document.getElementsByTagName('monopoly-trans-cash');
element.addEventListener('cash-transaction', someFunction);
function someFunction(event.detail) {
  // do something
}
```
**the detail we receive is something like this:**

```json
  {
    "to": "PABCDEF003",
    "from": "PABCDEF001",
    "amount": 345
  }
```
### LICENSE
**MIT**
### colaborators
@gmailm @hectorclaire @davidhdzhdz

## ¡GOOD HACK!
