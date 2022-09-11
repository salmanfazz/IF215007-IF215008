![Screenshot](https://user-images.githubusercontent.com/49604034/189536327-9dd01a6e-b056-455a-bda4-7bbeb94fcf7d.png)
```html
<html lang="en">
<head>
    <title>World of Warcaft - Database</title>
    <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.2.1/dist/css/bootstrap.min.css" rel="stylesheet" integrity="sha384-iYQeCzEYFbKjA/T2uDLTpkwGzCiq6soy8tYaI1GyVh/UjpbCx/TYkiZhlZB6+fzT" crossorigin="anonymous">
</head>
<body>

    <div class="container">
        <h1>List Item - World of Warcaft</h1>
        <div class="row">
            <div class="col">
                <form>
                    <div class="mb-3">
                        <label for="exampleInputEmail1" class="form-label">Item Name</label>
                        <input type="text" class="form-control" id="name">
                    </div>
                    <div class="mb-3">
                        <label for="exampleInputPassword1" class="form-label">Item Type</label>
                        <input type="text" class="form-control" id="type">
                    </div>
                    <div class="mb-3">
                        <label for="exampleInputPassword1" class="form-label">Amount</label>
                        <input type="text" class="form-control" id="amount">
                    </div>
                    <div class="mb-3">
                        <label for="exampleInputPassword1" class="form-label">Price</label>
                        <input type="text" class="form-control" id="price">
                    </div>
                    <button type="submit" class="btn btn-primary" id="submit">Submit</button>
                </form>
            </div>
        </div>
    </div>
    <div class="col">
        <table class="table table-striped">
            <thead>
                <tr>
                    <th scope="col">No.</th>
                    <th scope="col">Item Name</th>
                    <th scope="col">item Type</th>
                    <th scope="col">Amount</th>
                    <th scope="col">Price</th>
                </tr>
            </thead>
            <tbody id="list-item">
                
            </tbody>
        </table>
    </div>
    
    <script>
        function showItem() {
            const dataStore = localStorage.getItem("dataStore");
            var dataStoreObjectArray = JSON.parse(dataStore);
            if(dataStoreObjectArray === null) {
                dataStoreObjectArray = [];
            }

            const listItem = document.getElementById("list-item");

            let isilistItem = ``;

            dataStoreObjectArray.forEach(function(dataStoreObject, index) {
                isilistItem += `
                <tr>
                            <th scope="row">${index + 1}</th>
                            <td>${dataStoreObject.name}</td>
                            <td>${dataStoreObject.type}</td>
                            <td>${dataStoreObject.amount}</td>
                            <td>${dataStoreObject.price}</td>
                        </tr>
                `;
            });

            listItem.innerHTML = isilistItem;

        }

        showItem();

        var txtName = document.getElementById("name");
        var txtType = document.getElementById("type");
        var txtAmount = document.getElementById("amount");
        var txtPrice = document.getElementById("price");
        var buttonSubmit = document.getElementById("submit");

        buttonSubmit.onclick = function(onClickSubmitButton) {
            const name = txtName.value;
            const type = txtType.value;
            const amount = txtAmount.value;
            const price = txtPrice.value;
            const alert = `Successfull add item ${name} type ${type} with price ${price} and amount ${amount}pcs !`;
            const data = {
                name,
                type,
                amount,
                price,
            };

            console.log(data);

            const dataStore = localStorage.getItem("dataStore");
            const dataStoreObjectArray = JSON.parse(dataStore)

            if(dataStore === null) {
                localStorage.setItem("dataStore", JSON.stringify([data]));
            } else {
                dataStoreObjectArray.push(data);
                localStorage.setItem("dataStore", JSON.stringify(dataStoreObjectArray));
            }

            showItem();
        };

    </script>
</body>
</html>
```
