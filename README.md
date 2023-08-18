# PracticeWithBootStrap

<h2> Output </h2>

<!DOCTYPE html>

<!-- 1. Header and Introduction -->

<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <link rel="stylesheet" href="https://stackpath.bootstrapcdn.com/bootstrap/4.3.1/css/bootstrap.min.css">
    <style> 

        /* <!-- 4. Color Scheme utilizing custom CSS--> */
        /* Custom style - event's color scheme */
        .navbar {
            background-color: #123456;
        }
        .header-title {
            color: #654321;
        }
    </style>
</head>

<body>
    <nav class="navbar navbar-expand-lg navbar-dark">
        <a class="navbar-brand" href="#">
            <img src="https://img.freepik.com/free-vector/technology-conference-bannertemplate_1361-2226.jpg?w=1060&t=st=1692007435~exp=1692008035~hmac=4a320799476b44e13d237cf7b406451ef2f24f95dfd32508e6fd1ecab7a42f8a" alt="Event Logo" width="70" height="70"> Tech Conference
        </a>
    </nav>
    <div class="container mt-5">
        <h1 class="header-title">Welcome to the Tech Conference</h1>
        <p>An exciting event where technology leaders and enthusiasts come together.</p>
    </div>


    <!-- 2. Sessions Table -->

<div class="container mt-5">
    <h2 class="header-title">Conference Sessions</h2>
    <table class="table table-responsive-lg table-striped">
        <thead>
            <tr>
                <th>Session Name</th>
                <th>Speaker</th>
                <th>Date</th>
                <th>Time</th>
            </tr>
        </thead>
        <tbody>
            <tr>
                <td><a href="#" data-toggle="modal" data-target="#session1Modal">Session 1: Java</a></td>
                <td>Speaker 1</td>
                <td>20/12/2023</td>
                <td>10:00 AM</td>
            </tr>
            <tr>
                <td><a href="#" data-toggle="modal" data-target="#session1Modal">Session 2: MERN</a></td>
                <td>Speaker 2</td>
                <td>20/12/2023</td>
                <td>03:00 PM</td>
            </tr>
            <!-- More rows for other sessions -->
        </tbody>
    </table>
    
    <!-- 3. Registration Form -->

<div class="container mt-5">
    <h2 class="header-title">Register for the Conference</h2>
    <form id="registrationForm">
        <div class="form-group">
            <label for="name">Name:</label>
            <input type="text" class="form-control" id="name" placeholder="Enter your name" required>
        </div>
        <div class="form-group">
            <label for="email">Email:</label>
            <input type="email" class="form-control" id="email" placeholder="Enter your email" required>
        </div>
        <div class="form-group">
            <label for="organization">Organization:</label>
            <input type="text" class="form-control" id="organization" placeholder="Enter your organization">
        </div>
        <div class="form-group">
            <label for="sessions">Preferred Sessions:</label>
            <select class="form-control" id="sessions" multiple>
                <option>Session 1: Java</option>
                <option>Session 2: MERN</option>

                <!-- More sessions  -->

            </select>
        </div>

       
        
        <!-- 5. Submit Button and Success Message -->
        <!-- inside the registration form... -->
        <button type="submit" class="btn btn-primary mb-3" id="submitBtn">Submit</button>

        <!-- Success Modal -->
        <div class="modal fade" id="successModal" tabindex="-1" role="dialog">
            <div class="modal-dialog" role="document">
                <div class="modal-content">
                    <div class="modal-header">
                        <h5 class="modal-title">Success</h5>
                        <button type="button" class="close" data-dismiss="modal" aria-label="Close">
                            <span aria-hidden="true">&times;</span>
                        </button>
                    </div>
                    <div class="modal-body">
                        <p>Thank you for registering! We look forward to seeing you at the conference.</p>
                    </div>
                    <div class="modal-footer">
                        <button type="button" class="btn btn-secondary" data-dismiss="modal">Close</button>
                    </div>
                </div>
            </div>
        </div>

        <!-- JavaScript to handle form submission -->
        <script src="https://code.jquery.com/jquery-3.3.1.slim.min.js"></script>
        <script src="https://cdnjs.cloudflare.com/ajax/libs/popper.js/1.14.7/umd/popper.min.js"></script>
        <script src="https://stackpath.bootstrapcdn.com/bootstrap/4.3.1/js/bootstrap.min.js"></script>
        <script>
            $('#registrationForm').on('submit', function (e) {
                e.preventDefault();
                var name = $('#name').val().trim();
                var email = $('#email').val().trim();

                if (name === '' || email === '') {
                    alert('Name and Email are required fields!');
                    return;
                }
                $('#successModal').modal('show'); // Show the success modal
             });
        </script>

     </form>
    </div>
   </div>
</body>

<!-- 6. Footer... -->
<footer class="bg-dark text-white mt-5">
    <div class="container pt-4">
        <div class="row">
            <div class="col-md-4">
                <h5>About the Event</h5>
                <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Iure dicta obcaecati corrupti deleniti, saepe ullam sequi voluptatem accusamus similique quam ipsa ea maiores recusandae sapiente officiis voluptatum optio unde reiciendis!.</p>
            </div>
            <div class="col-md-4">
                <h5>Contact Us</h5>
                <p>Email: info@techconference.com</p>
                <p>Phone: +1234567890</p>
            </div>
            <div class="col-md-4">
                <h5>Follow Us</h5>
                <a href="#" class="text-white">Facebook</a><br>
                <a href="#" class="text-white">Twitter</a><br>
                <a href="#" class="text-white">LinkedIn</a>
            </div>
        </div>
    </div>
</footer>


</html>
