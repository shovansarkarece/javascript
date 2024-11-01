# Dom_Project
```
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>JSON to Invoice</title>
    <style>
        /* Basic Styling for the Invoice */
        body {
            font-family: Arial, sans-serif;
            margin: 20px;
            background-color: #f4f4f4;
        }
        .invoice-container {
            max-width: 800px;
            margin: auto;
            background: #fff;
            padding: 20px;
            border-radius: 8px;
            box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
        }
        .invoice-header {
            text-align: center;
            margin-bottom: 20px;
        }
        .invoice-header h1 {
            margin: 0;
        }
        .client-info, .invoice-details {
            margin-bottom: 20px;
        }
        .invoice-details table, .items-table {
            width: 100%;
            border-collapse: collapse;
        }
        .invoice-details th, .invoice-details td,
        .items-table th, .items-table td {
            border: 1px solid #ddd;
            padding: 8px;
            text-align: left;
        }
        .invoice-details th, .items-table th {
            background-color: #f2f2f2;
        }
        .total {
            text-align: right;
            margin-top: 20px;
            font-size: 1.2em;
        }
        .notes {
            margin-top: 20px;
        }
    </style>
</head>
<body>
    <div class="invoice-container" id="invoice">
        <!-- Invoice Header -->
        <div class="invoice-header">
            <h1 id="invoiceTitle"></h1>
        </div>

        <!-- Invoice Details -->
        <div class="invoice-details">
            <table>
                <tbody>
                    <tr>
                        <th>Invoice Number:</th>
                        <td id="invoiceNumber"></td>
                    </tr>
                    <tr>
                        <th>Date:</th>
                        <td id="invoiceDate"></td>
                    </tr>
                    <tr>
                        <th>Due Date:</th>
                        <td id="invoiceDueDate"></td>
                    </tr>
                </tbody>
            </table>
        </div>

        <!-- Client Information -->
        <div class="client-info">
            <h2>Bill To:</h2>
            <p id="clientName"></p>
            <p id="clientAddress"></p>
        </div>

        <!-- Items Table -->
        <div class="items">
            <table class="items-table">
                <thead>
                    <tr>
                        <th>Description</th>
                        <th>Quantity</th>
                        <th>Unit Price</th>
                        <th>Total</th>
                    </tr>
                </thead>
                <tbody id="itemsBody">
                    <!-- Dynamic Invoice Items Will Be Injected Here -->
                </tbody>
            </table>
        </div>

        <!-- Grand Total -->
        <div class="total" id="grandTotal">
            Grand Total: $0.00
        </div>

        <!-- Notes -->
        <div class="notes">
            <h3>Notes:</h3>
            <p id="invoiceNotes"></p>
        </div>
    </div>

    <script>
        const invoiceData = {
            "title": "Invoice From Office Supplies",
            "invoiceNumber": "INV-1001",
            "date": "2023-10-01",
            "dueDate": "2023-10-15",
            "client": {
                "name": "Jane Doe",
                "address": "1234 Elm Street, Springfield, USA"
            },
            "items": [
                {
                    "description": "Web Design Services",
                    "quantity": 10,
                    "unitPrice": 50
                },
                {
                    "description": "Hosting (1 year)",
                    "quantity": 1,
                    "unitPrice": 100
                },
                {
                    "description": "Domain Name (1 year)",
                    "quantity": 1,
                    "unitPrice": 10
                },
                {
                    "description": "Service X",
                    "quantity": 1,
                    "unitPrice": 100
                },
            ],
            "notes": "Thank you for your business!"
        };

        function populateCommonItems(){
            document.getElementById('invoiceTitle').innerText = invoiceData.title;
            document.getElementById('invoiceNumber').innerText = invoiceData.invoiceNumber;
            document.getElementById('invoiceDate').textContent = invoiceData.date;
            document.getElementById('invoiceDueDate').textContent = invoiceData.dueDate;
            document.getElementById('clientName').textContent = invoiceData.client.name;
            document.getElementById('clientAddress').textContent = invoiceData.client.address;
            document.getElementById('invoiceNotes').textContent = invoiceData.notes;
        }

        function populateItems(){
            const itemsBody = document.getElementById('itemsBody');
            let grandTotal = 0;
            invoiceData.items.forEach(item=>{
                console.log(item);
                const row = document.createElement('tr');
                row.innerHTML = `<td>${item.description}</td>
                                <td>${item.quantity}</td>
                                <td>${item.unitPrice}</td>
                                <td>${item.quantity * item.unitPrice}</td>`;
                itemsBody.appendChild(row);
                grandTotal += item.quantity * item.unitPrice

                document.getElementById('grandTotal').innerHTML = `Grand Total: $${grandTotal}`;
            })
        }

        populateCommonItems();
        populateItems();
    </script>
</body>
</html>
```
### Output
![image](https://github.com/user-attachments/assets/b58a4fc7-37db-4bbf-a0b8-27be7839dbd3)
