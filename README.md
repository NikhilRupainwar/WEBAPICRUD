# WEBAPICRUD
// search
    function find2() {
        var id = $('#custId').val();
        $.getJSON(uri + '/' + id)
            .done(function (data) {
                document.getElementById('newCustomerid').value = data.CustomerID;
                document.getElementById('newCustomerName').value = data.CustomerName;
                document.getElementById('newCustomerAddress').value = data.CustomerAddress;
                document.getElementById('newCustomerCity').value = data.CustomerCity;
            })
            .fail(function (jqXHR, textStatus, err) {
                $('#Customers1').text('Error: ' + err);
            });
    }
