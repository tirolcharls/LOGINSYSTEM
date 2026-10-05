=====================================================
 FOTO LOGIN SYSTEM - README
=====================================================

FILES IN THIS FOLDER
--------------------
index.html            Main login page (Student + Photo Journalist tabs)
forgot-password.html  Forgot password page
signup.html           Create new journalist account page
style.css             ALL colours, fonts, spacing and hover effects
README.txt            This file

IMPORTANT: Keep all files together in the SAME folder.
The pages find each other and style.css by file name.


HOW TO OPEN IN VISUAL STUDIO CODE
---------------------------------
1. Open Visual Studio Code.
2. Click File > Open Folder...
3. Choose the folder "foto-login-system" and click Select Folder.
4. Click a file on the left side to edit it.

HOW TO SEE THE PAGE
-------------------
- Right-click index.html in your folder and choose Open With > your browser.
  (Or double-click it.) index.html is the MAIN file.
- After you edit and save a file (Ctrl + S), refresh the browser (F5).
- When you add PHP, the pages must run on a server such as XAMPP.
  Put the folder inside htdocs, then open:
  http://localhost/foto-login-system/index.html


WHERE TO PUT YOUR PHP LINKS
---------------------------
Each spot is marked with a comment that starts with "PHP:".
Just type your file name between the two quote marks.

index.html
  Line 29  <a class="btn-blue" href="">Enter Gallery</a>
           -> Student button. Example: href="gallery.php"
  Line 34  <form ... action="" method="POST">
           -> Photo Journalist login. Example: action="login.php"

forgot-password.html
  Line 23  <form ... action="" method="POST">
           -> Send Reset Link. Example: action="send-reset.php"

signup.html
  Line 23  <form ... action="" method="POST">
           -> Create Account. Example: action="register.php"

Field names your PHP will read with $_POST:
  Login:      username, password
  Forgot:     email
  Sign up:    username, email, password, confirm_password

Links between the pages already work:
  Forgot Password -> forgot-password.html
  Sign up         -> signup.html
  Back to Login / Log in -> index.html


COLOURS YOU CAN CHANGE FIRST
----------------------------
Open style.css. The colours are at the very top under "- COLOURS -".
Change the code after the colon (example: #2563eb).

  --blue          Active tab and all big buttons
  --blue-hover    Button colour when the mouse is over it
  --bg-dark       Darkest part of the background
  --bg-mid        Middle blue of the background
  --bg-glow       Soft glow at the top-right
  --card-bg       The centre box
  --tab-inactive  The tab that is not selected
  --link-color    "Sign up" and "Log in" links


SCHOOL LOGO (shows on every page)
---------------------------------
logo.png is the Cordova Public College logo with a transparent background.
It appears faded behind the box on all 3 pages.
In style.css, find the part called "SCHOOL LOGO":
  width / height   -> how big the logo is
  opacity          -> how faded it is (0.2 now; try 0.1 to 0.3)
To use a different logo, replace logo.png (keep the same name).
