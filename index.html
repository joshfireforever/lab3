<!DOCTYPE html>
<html>
    <head>
        <title> Sign Up Page </title>
        <link rel="stylesheet" href="https://stackpath.bootstrapcdn.com/bootstrap/4.5.2/css/bootstrap.min.css" integrity="sha384-JcKb8q3iqJ61gNV9KGb8thSsNjpSL0n8PARn9HuZOnIxN0hoP+VmmDGMN5t9UJ0Z" crossorigin="anonymous">
        <link rel="stylesheet" href="css/style.css">
        <link href="https://fonts.googleapis.com/css2?family=Spartan:wght@100;300&display=swap" rel="stylesheet">
        <script src="https://ajax.googleapis.com/ajax/libs/jquery/3.5.1/jquery.min.js"></script>
    </head>
    
    <body>
        <br>
        <h1> Sign Up </h1>
        <br>
        <form id="signupForm" action="welcome.html">
            <div id="fields">
            First Name: <input type="text"  name="fName" class="form-control">
            Last Name:  <input type="text"  name="lName" class="form-control">
            Gender: &nbsp
                <input type="radio" name="gender" value="m"> Male   &nbsp
                <input type="radio" name="gender" value="f"> Female <br>
            Zip Code:  <input type="text" name="zip" id="zip" class="form-control">
                        <div id="zipError"></div>
            City:      <span id="city"></span><br>
            Latitude:  <span id="latitude"></span><br>
            Longitude: <span id="longitude"></span><br>
           
            State: &nbsp
            <select id="state" name="state">
               <option> Select One </option>
            </select><br>
            
            Select a County: &nbsp<select id="county" name="county"></select><br>
            
            Desired Username: <input type="text" id="username" name="username" class="form-control" aria-label="Username">
                              <div id="usernameError"></div>
            Password:         <input type="password" id="password" name="password" class="form-control">
                              <div id="passwordError"></div>
            Password Again:   <input type="password" id="passwordAgain" class="form-control">
                              <div id="passwordAgainError"></div>
            </div>
            <div id="button"><input type="submit" value="Sign up!" class="btn btn-outline-primary"></div>
        </form>
        
        <script>
        $(document).ready(function() {
            /*global $*/
            /*global fetch*/
            
            populateStates();
            let tempAbbr = "";
            
            async function populateStates () {
                let stateURL = "https://cst336.herokuapp.com/projects/api/state_abbrAPI.php";
                let response = await fetch(stateURL);
                let data = await response.json();

                data.forEach( function(i){ 
                    $("#state").append(`<option value="${i.usps}"> ${i.state} </option>`);
                });
            }
            
            var usernameAvailable = false;
            var selectedCounty = "";
                    
            //Displaying City from API after typing a zip code    
            $("#zip").on("change", async function() {
                    
                //alert(  $("#zip").val()  );
                let zipCode = $("#zip").val();
                let url = `https://cst336.herokuapp.com/projects/api/cityInfoAPI.php?zip=${zipCode}`;
                let response = await fetch(url);
                let data = await response.json();
                
                if (!data) {
                    $("#zipError").html("&nbsp&nbspZip code not found!");
                    $("#zipError").attr("class", "bg-danger text-white");
                    return;
                }
                else {
                    $("#zipError").empty();
                }
                
                //console.log(data);
                $("#city").html(data.city);
                $("#latitude").html(data.latitude);
                $("#longitude").html(data.longitude);
                selectedCounty = data.county;
                
                let stateURL = "https://cst336.herokuapp.com/projects/api/state_abbrAPI.php";
                let stateResponse = await fetch(stateURL);
                let stateData = await stateResponse.json();
                let tempStr = "";
                
                stateData.forEach( function(i) { 
                    if (data.state == i.usps) {
                        $('[name=state]').val(`${i.usps}`);
                        $("#state").change();
                        return;
                    }
                });
            });//zip
             
            $("#state").on("change", async function() {
                    
                //alert(  $("#state").val()  );
                let state = $("#state").val();
                $("#county").empty();
                let url = `https://cst336.herokuapp.com/projects/api/countyListAPI.php?state=${state}`;
                let response = await fetch(url);
                let data = await response.json();
                //console.log(data);
                data.forEach( function(i){ 
                    $("#county").append(`<option> ${i.county} </option>`);
                    if (selectedCounty == i.county) {
                        $('[name=county]').val(`${i.county}`);
                    }
                });

            });//state
            
            $("#username").on("change", async function() {
                    
                //alert(  $("#username").val()  );
                let username = $("#username").val();
                let url = `https://cst336.herokuapp.com/projects/api/usernamesAPI.php?username=${username}`;
                let response = await fetch(url);
                let data = await response.json();
                
                if (data.available) {
                    $("#usernameError").html("Username available!");
                    $("#usernameError").attr("class", "bg-success text-white");
                    usernameAvailable = true;
                }
                else {
                    $("#usernameError").html("Username not available!");
                    $("#usernameError").attr("class", "bg-danger text-white");
                    usernameAvailable = false;
                }

            });//username
            
            $("#signupForm").submit(function(e) {
           
                //alert("submitting form...");
                if (!isFormValid()) {
                    e.preventDefault();
                }
                
                function isFormValid() {
                    
                    var isValid = true;
                    
                    //Username Checking
                    if (!usernameAvailable) {
                      isValid = false;
                    }
                    
                    if ($("#username").val().length == 0) {
                        isValid = false;
                        $("#usernameError").html("Username is required!");
                        $("#usernameError").attr("class", "bg-danger text-white");
                    }
                  
                    //Password Checking
                    if ($("#password").val().length < 6 ) {
                        $("#passwordError").html("Enter a password of at least 6 characters!");
                        $("#passwordError").attr("class", "bg-danger text-white");
                        isValid = false;
                    }
                    else if ($("#password").val() != $("#passwordAgain").val()) {
                        $("#passwordError").empty();
                        $("#passwordAgainError").html("Password Mismatch!");
                        $("#passwordAgainError").attr("class", "bg-danger text-white");
                        isValid = false;
                    }
                    else {
                        $("#passwordError").empty();
                        $("#passwordAgainError").empty();
                    }
                    
                    return isValid;
                }
               
            });//signupForm
        });
        </script>
    </body>
</html>