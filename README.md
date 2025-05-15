<!DOCTYPE html>
<html lang="id">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Registration Form</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            margin: 0;
            padding: 0;
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
            background: url('chase atlantic concert📸 (1).jpg') no-repeat center center fixed;
            background-size: cover;
        }
        .blur-box{
            position: absolute;
            top: 40%;
            left: 5%;
            width: 200px;
            backdrop-filter: blur(10px);
            color: #ffffff;
            font-size: 15px;
            font-weight: bold;
            font-family: arial, sans-serif;
            padding: 10px;
            text-align: center;
            border-radius: 15px;
            box-shadow: 0 4px 6px rgba(0, 0, 0, 0.2);
        }
        @media (max-width: 600px) {
            .blur-box {
                width: 150px;
                top: 30%;
                left: 10%;
            }
        }

        /* Media query for screens larger than 600px */
        @media (min-width: 601px) {
            .blur-box {
                width: 300px;
                top: 40%;
                left: 5%;
            }
        }
        .container {
            background: rgba(255, 255, 255, 255, 0.1);
            backdrop-filter: blur(20px);
            padding: 15px 40px;
            border-radius: 15px;
            margin: 50px 5% 50px auto;
            width: 300px;
            font-size: 12px;
            box-shadow: 0 4px 6px rgba(0, 0, 0, 0.2);
        }
        @media (max-width: 768px) {
            .container {
                width: 100%;
                padding: 0 20px;
            }
        }
        h2 {
            text-align: center;
            margin-bottom: 10px;
            color: rgb(255, 255, 255);
        }
        label {
            display: block;
            margin-bottom: 3px;
            font-weight: bold;
            color: white;
        }
        input, select, textarea, button {
            width: 100%;
            padding: 7px;
            margin-bottom: 5px;
            border: 1px solid #ffffff;
            border-radius: 10px;
            font-size: 12px;
        }
        input::placeholder, textarea::placeholder {
            color: #8362a6;
            font-style: italic;
        }
        input[type="radio"] {
            width: auto;
            margin-right: 1px;
        }
        .radio-group {
            display: flex;
            align-items: center;
            gap: 5px;
            margin-bottom: 5px;
        }
        .separator {
            border-top: 1px solid white;
            margin-bottom: 15px;
        }
        button {
            background: #a42bbf;
            color: rgb(255, 255, 255);
            font-weight: bold;
            cursor: pointer;
            transition: background 0.3s ease;
            border: none;
            border-radius: 10px;
            padding: 10px 130px;
            width: auto;
            display: block;
            margin: auto;
        }
        button:hover {
            background: #ddbbe3;
        }
    </style>
</head>
<body>
    <div class="blur-box">
        <p>Registration Form by Dwiyanti Annisa Suangga</p>
    </div>
    <div class="container" id="form-login">
        <h2>Registration Form</h2>
        <form id="Registration-form">
            <label for="name">Full Name:</label>
            <input type="text" id="name" name="name" placeholder="Enter your full name" required>

            <label for="email">E-mail:</label>
            <input type="email" id="email" name="email" placeholder="Enter your email" required>

            <label for="agama">Religion:</label>
            <select id="agama" name="agama" required>
                <option value="" disabled selected>Select religion</option>
                <option value="Islam">Islam</option>
                <option value="kristen">Christian</option>
                <option value="katolik">Catholic</option>
                <option value="Hindu">Hindu</option>
                <option value="Buddha">Buddhist</option>
                <option value="konghucu">Confucian</option>
                <option value="ateis">No religion</option>
            </select>

            <label for="tanggal">Date of birth:</label>
            <input type="date" id="tanggal" name="tanggal" placeholder="Select date of birth" required>

            <label for="alamat">Address:</label>
            <input type="text" id="alamat" name="alamat" placeholder="Enter your address" required>

            <label for="deskripsi">Self-description:</label>
            <textarea id="deskripsi" name="deskripsi" placeholder="Describe yourself" rows="3"></textarea>

            <label>Gender:</label>
            <div class="radio-group">
                <input type="radio" id="laki-laki" name="jenis_kelamin" value="Laki-Laki" required>
                <label for="laki-laki">Male</label>
                <input type="radio" id="perempuan" name="jenis_kelamin" value="Perempuan" required>
                <label for="perempuan">Female</label>
            </div>

            <div class="separator"></div>

            <button type="submit">Register</button>
        </form>
    </div>
    <script>
    document.querySelector("#Registration-form").addEventListener("submit", function (e) {
    e.preventDefault();
    
    const name = document.querySelector("#name").value.trim();
    const email = document.querySelector("#email").value.trim();
    const agama = document.querySelector("#agama").value.trim();
    const tanggal = document.querySelector("#tanggal").value.trim();
    const alamat = document.querySelector("#alamat").value.trim();
    const deskripsi = document.querySelector("#deskripsi").value.trim();
    const gender = document.querySelector('input[name="jenis_kelamin"]:checked');

    if (!name || !email || !agama || !tanggal || !alamat || !deskripsi || !gender) {
        return;
    }

    localStorage.setItem("username",name);
    localStorage.setItem("useremail",email);
    localStorage.setItem("useragama",agama);
    localStorage.setItem("useralamat",alamat);
    localStorage.setItem("userdeskripsi",deskripsi);

    window.location.href = "DWIYANTI_004_D_SOAL2.html";
});
    </script>
</body>
</html>
