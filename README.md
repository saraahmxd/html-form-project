<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>User Information Form</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      margin: 20px;
      max-width: 900px;
    }

    form {
      display: grid;
      grid-template-columns: 200px 1fr;
      gap: 12px 20px;
      align-items: center;
    }

    h2 {
      grid-column: 1 / span 2;
      text-align: center;
      margin-bottom: 20px;
    }

    textarea {
      width: 100%;
    }

    .full-width {
      grid-column: 1 / span 2;
    }

    .buttons {
      grid-column: 1 / span 2;
      text-align: center;
      margin-top: 20px;
    }

    #footer {
      margin-top: 40px;
      padding: 15px;
      background-color: #f0f0f0;
      text-align: center;
      border-top: 2px solid #ccc;
    }

    #footer button {
      margin-top: 10px;
      padding: 8px 15px;
      cursor: pointer;
    }
  </style>
</head>
<body>
  <!-- HEADER -->
  <div id="header">
    <h2>InspireHealth Medical - Patient Information Form</h2>
  </div>

  <!-- MAIN FORM -->
  <form action="thankyou.html">
    <!-- Name -->
    <label for="fname">First Name:</label>
    <input type="text" id="fname" name="fname" maxlength="30" required>

    <label for="minit">Middle Initial:</label>
    <input type="text" id="minit" name="minit" maxlength="1">

    <label for="lname">Last Name:</label>
    <input type="text" id="lname" name="lname" maxlength="30" required>

    <!-- DOB -->
    <label for="dob">Date of Birth:</label>
    <input type="text" id="dob" name="dob" placeholder="MM/DD/YYYY" pattern="\d{2}/\d{2}/\d{4}">

    <!-- SSN -->
    <label for="ssn">Social Security #:</label>
    <input type="password" id="ssn" name="ssn" maxlength="11" placeholder="XXX-XX-XXXX">

    <!-- Address -->
    <label for="addr1">Address Line 1:</label>
    <input type="text" id="addr1" name="addr1" maxlength="30">

    <label for="addr2">Address Line 2:</label>
    <input type="text" id="addr2" name="addr2" maxlength="30">

    <label for="city">City:</label>
    <input type="text" id="city" name="city" maxlength="30">

    <label for="state">State:</label>
    <select id="state" name="state" required>
      <option value="">Select...</option>
      <option value="AL">Alabama</option>
      <option value="AK">Alaska</option>
      <option value="AZ">Arizona</option>
      <option value="AR">Arkansas</option>
      <option value="CA">California</option>
      <option value="CO">Colorado</option>
      <option value="CT">Connecticut</option>
      <option value="DE">Delaware</option>
      <option value="DC">District of Columbia</option>
      <option value="FL">Florida</option>
      <option value="GA">Georgia</option>
      <option value="HI">Hawaii</option>
      <option value="ID">Idaho</option>
      <option value="IL">Illinois</option>
      <option value="IN">Indiana</option>
      <option value="IA">Iowa</option>
      <option value="KS">Kansas</option>
      <option value="KY">Kentucky</option>
      <option value="LA">Louisiana</option>
      <option value="ME">Maine</option>
      <option value="MD">Maryland</option>
      <option value="MA">Massachusetts</option>
      <option value="MI">Michigan</option>
      <option value="MN">Minnesota</option>
      <option value="MS">Mississippi</option>
      <option value="MO">Missouri</option>
      <option value="MT">Montana</option>
      <option value="NE">Nebraska</option>
      <option value="NV">Nevada</option>
      <option value="NH">New Hampshire</option>
      <option value="NJ">New Jersey</option>
      <option value="NM">New Mexico</option>
      <option value="NY">New York</option>
      <option value="NC">North Carolina</option>
      <option value="ND">North Dakota</option>
      <option value="OH">Ohio</option>
      <option value="OK">Oklahoma</option>
      <option value="OR">Oregon</option>
      <option value="PA">Pennsylvania</option>
      <option value="PR">Puerto Rico</option>
      <option value="RI">Rhode Island</option>
      <option value="SC">South Carolina</option>
      <option value="SD">South Dakota</option>
      <option value="TN">Tennessee</option>
      <option value="TX">Texas</option>
      <option value="UT">Utah</option>
      <option value="VT">Vermont</option>
      <option value="VA">Virginia</option>
      <option value="WA">Washington</option>
      <option value="WV">West Virginia</option>
      <option value="WI">Wisconsin</option>
      <option value="WY">Wyoming</option>
    </select>

    <label for="zip">Zip Code:</label>
    <input type="text" id="zip" name="zip" pattern="\d{5,10}">

    <!-- Email -->
    <label for="email">Email:</label>
    <input type="email" id="email" name="email">

    <!-- Textarea -->
    <label for="symptoms">Describe Symptoms:</label>
    <textarea id="symptoms" name="symptoms" rows="3" cols="50"></textarea>

    <!-- Checkboxes -->
    <p class="full-width">Check all that apply:</p>
    <div class="full-width">
      <input type="checkbox" id="cp" name="history" value="Chicken Pox">
      <label for="cp">Chicken Pox</label>
      <input type="checkbox" id="me" name="history" value="Measles">
      <label for="me">Measles</label>
      <input type="checkbox" id="cv" name="history" value="Covid-19">
      <label for="cv">Covid-19</label>
      <input type="checkbox" id="sp" name="history" value="Small Pox">
      <label for="sp">Small Pox</label>
      <input type="checkbox" id="tt" name="history" value="Tetanus">
      <label for="tt">Tetanus</label>
    </div>

    <!-- Radio buttons -->
    <p class="full-width">Gender:</p>
    <div class="full-width">
      <input type="radio" id="male" name="gender" value="Male">
      <label for="male">Male</label>
      <input type="radio" id="female" name="gender" value="Female">
      <label for="female">Female</label>
      <input type="radio" id="other" name="gender" value="Other">
      <label for="other">Other</label>
    </div>

    <p class="full-width">Have you been vaccinated?</p>
    <div class="full-width">
      <input type="radio" id="vac_yes" name="vaccinated" value="Yes">
      <label for="vac_yes">Yes</label>
      <input type="radio" id="vac_no" name="vaccinated" value="No">
      <label for="vac_no">No</label>
    </div>

    <p class="full-width">Do you have insurance?</p>
    <div class="full-width">
      <input type="radio" id="ins_yes" name="insurance" value="Yes">
      <label for="ins_yes">Yes</label>
      <input type="radio" id="ins_no" name="insurance" value="No">
      <label for="ins_no">No</label>
    </div>

    <!-- Slider -->
    <label for="health">Health Scale (1-10):</label>
    <input type="range" id="health" name="health" min="1" max="10">

    <!-- Username & Password -->
    <label for="userid">Desired User ID:</label>
    <input type="text" id="userid" name="userid" maxlength="20">

    <label for="pwd">Password:</label>
    <input type="password" id="pwd" name="pwd" maxlength="20">

    <label for="pwd2">Re-enter Password:</label>
    <input type="password" id="pwd2" name="pwd2" maxlength="20">

    <!-- Buttons -->
    <div class="buttons">
      <button type="reset">CLEAR AND START OVER</button>
      <button type="submit">Submit</button>
    </div>
  </form>

  <!-- FOOTER -->
  <div id="footer">
    <p>InspireHealth Medical | CONTACT US | FB / Twitter / Instagram</p>
    <p>PO BOX 63737, Houston TX 77001</p>
    <button onclick="alert('Contact form coming soon!')">Contact Us</button>
  </div>
</body>
</html>
