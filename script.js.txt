function idCard() {
    // Pull in input values
    let firstName = document.getElementById('firstName').value;
    let lastName = document.getElementById('lastName').value;
    let address = document.getElementById('address').value;

    // Post full name and address to ID card
    document.getElementById('postFullName').innerHTML = firstName + ' ' + lastName;
    document.getElementById('postAddress').innerHTML = "Address: " + address;

    // Pull in numeric inputs
    let age = Number(document.getElementById('age').value);
    let phoneNumber = document.getElementById('phoneNumber').value;

    // Create array and push numbers
    let numberArray = [];
    numberArray.push(age);
    numberArray.push(phoneNumber);

    // Loop through array and display
    for (let i = 0; i < numberArray.length; i++) {
        if (numberArray[i] <= 100) {
            document.getElementById('postAge').innerHTML = "Age: " + age;
        } else if (numberArray[i] > 100) {
            document.getElementById('postPhone').innerHTML = "Phone Number: " + phoneNumber;
        }
    }
}
