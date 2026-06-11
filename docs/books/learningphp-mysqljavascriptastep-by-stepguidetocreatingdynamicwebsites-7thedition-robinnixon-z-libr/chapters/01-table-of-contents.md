# Table of Contents

**Preface. . . . xix**

**1. Introduction to Dynamic Web Content. . . . .**

HTTP and HTML: Berners-Lee’s Basics 2

The Request/Response Procedure 3

The Benefits of PHP, MySQL, JavaScript, CSS, and HTML 5

MariaDB: The MySQL Clone 6

Using PHP 7

Using MySQL 8

Using JavaScript 9

Using CSS 10

And Then There’s HTML5 11

The Apache Web Server 12

Node.js: An Alternative to Apache 13

About Open Source 14

Bringing It All Together 14

Questions 16

**2. Setting Up a Development Server. . . . . 17**

What Is a WAMP, MAMP, or LAMP? 18

Installing AMPPS on Windows 18

Testing the Installation 23

Accessing the Document Root (Windows) 25

Alternative WAMPs 26

Installing AMPPS on macOS 27

Installing a LAMP on Linux 29

Working Remotely 29

Logging In 29

Transferring Files 30

Using a Code Editor 31

Questions 32

**3. Introduction to PHP. . . . . . 33**

Incorporating PHP Within HTML 33

This Book’s Examples 35

The Structure of PHP 35

Using Comments 35

Basic Syntax 36

Variables 37

Operators 42

Variable Assignment 46

Multiline Strings 49

Variable Typing 52

Constants 53

Predefined Constants 53

The Difference Between the echo and print Commands 54

Functions 55

Variable Scope 56

Questions 62

**4. Expressions and Control Flow in PHP. . . . . 63**

Expressions 63

TRUE or FALSE? 64

Literals and Variables 65

Operators 66

Operator Precedence 67

Associativity 69

Relational Operators 70

Conditionals 74

The if Statement 75

The else Statement 76

The elseif Statement 78

The switch Statement 79

The ? (or Ternary) Operator 82

Looping 83

while Loops 84

do...while Loops 86

for Loops 86

Breaking Out of a Loop 88

The continue Statement 89

Implicit and Explicit Casting 90

PHP Modularization 91

Questions 92

**5. PHP Functions and Objects. . . . . 93**

PHP Functions 94

Defining a Function 96

Returning a Value 96

Returning an Array 98

Returning Global Variables 98

Recap of Variable Scope 99

Including and Requiring Files 99

The include Statement 100

Using include\_once 100

Using require and require\_once 101

PHP Version Compatibility 101

PHP Objects 102

Terminology 102

Declaring a Class 104

Creating an Object 105

Accessing Objects 105

Cloning Objects 106

Constructors 108

Destructors 108

Writing Methods 109

Declaring Properties 110

Static Methods 110

Declaring Constants 111

Property and Method Scope 112

Static Properties 113

Inheritance 114

Questions 118

**6. PHP Arrays. . . . . 119**

Basic Access 119

Numerically Indexed Arrays 119

Associative Arrays 121

Assignment Using the array Keyword 122

The foreach...as Loop 123

Multidimensional Arrays 125

Using Array Functions 129

is\_array 129

count 129

sort 129

shuffle 130

explode 130

compact 131

reset 132

end 133

Questions 133

**7. Practical PHP. . . . 135**

Using printf 135

Precision Setting 137

String Padding 138

Using sprintf 139

Date and Time Functions 140

Date Constants 142

Using checkdate 143

File Handling 143

Checking Whether a File Exists 143

Creating a File 144

Reading from Files 145

Copying Files 146

Moving a File 147

Deleting a File 147

Updating Files 148

Locking Files for Multiple Accesses 149

Reading an Entire File 151

Uploading Files 152

System Calls 157

Questions 159

**8. Introduction to MySQL. . . . 161**

MySQL Basics 161

Key Database Terms 162

Accessing MySQL via the Command Line 162

Starting the Command-Line Interface 163

Using the Command-Line Interface 167

MySQL Commands 168

Data Types 173

Indexes 184

Creating an Index 184

Querying a MySQL Database 190

Joining Tables 201

Using Logical Operators 204

MySQL Functions 205

Accessing MySQL via phpMyAdmin 205

Questions 207

**9. Mastering MySQL. . . . . . . . . . 209**

Database Design 209

Primary Keys: The Keys to Relational Databases 210

Normalization 211

First Normal Form 212

Second Normal Form 214

Third Normal Form 217

When Not to Use Normalization 219

Relationships 219

One-to-One 220

One-to-Many 220

Many-to-Many 221

Databases and Privacy 223

Transactions 223

Transaction Storage Engines 223

Using START TRANSACTION 225

Using COMMIT 225

Using ROLLBACK 225

Using EXPLAIN 226

Backing Up and Restoring 228

Using mysqldump 228

Creating a Backup File 230

Restoring from a Backup File 232

Dumping Data in CSV Format 233

Planning Your Backups 233

Questions 234

**10. Accessing MySQL Using PHP. . . . 235**

Querying a MySQL Database with PHP 235

The Process 235

Creating a Login File 236

Connecting to a MySQL Database 238

Building and Executing a Query 239  
Fetching a Result 239  
Fetching a Row While Specifying the Style 241  
Closing a Connection 242  
A Practical Example 243  
The \$\_POST Array 246  
Deleting a Record 247  
Displaying the Form 247  
Querying the Database 248  
Running the Program 249  
Practical MySQL 250  
Creating a Table 250  
Describing a Table 251  
Dropping a Table 252  
Adding Data 253  
Retrieving Data 254  
Updating Data 255  
Deleting Data 255  
Using AUTO\_INCREMENT 256  
Performing Additional Queries 257  
Preventing Hacking Attempts 259  
Steps You Can Take 260  
Using Placeholders 261  
Preventing JavaScript Injection into HTML 264  
Questions 266

11. Form Handling. . . . . . 267

Building Forms 267

Retrieving Submitted Data 269

Default Values 270

Input Types 271

Sanitizing Input 283

An Example Program 284

Questions 287

12. Cookies, Sessions, and Authentication. . . . . . 289

Using Cookies in PHP 289

Setting a Cookie 291

Accessing a Cookie 292

Destroying a Cookie 292

HTTP Authentication 292

Storing Usernames and Passwords 296

An Example Program 298

Using Sessions 301

Starting a Session 302

Ending a Session 304

Setting a Timeout 305

Session Security 306

Questions 309

**13. Exploring JavaScript. . . . . . . . 311**

Outputting the Results 312

Using console.log 312

Using alert 312

Writing into Elements 312

Using document.write 312

JavaScript and HTML Text 313

Using Scripts Within a Document Head 315

Including JavaScript Files 315

Debugging JavaScript Errors 316

Using Comments 316

Semicolons 317

Variables 317

String Variables 318

Numeric Variables 318

Arrays 318

Operators 319

Arithmetic Operators 319

Assignment Operators 320

Comparison Operators 320

Logical Operators 321

Incrementing, Decrementing, and Shorthand Assignment 321

String Concatenation 321

Escape Characters 322

Variable Typing 322

Functions 324

Global Variables 324

Local Variables 325

Using let 326

Using const 327

The Document Object Model 328

Another Use for the \$ Symbol 330

Using the DOM 330

Questions 332

**14. Expressions and Control Flow in JavaScript. . . . . . . . 333**

Expressions 333

Literals and Variables 334

Operators 335

Operator Precedence 336

Associativity 337

Relational Operators 337

Using onerror 342

Using try...catch 343

Conditionals 344

The if Statement 344

The else Statement 344

The switch Statement 345

The ? Operator 347

Looping 347

while Loops 348

do...while Loops 348

for Loops 349

Breaking Out of a Loop 350

The continue Statement 351

Explicit Casting 351

Questions 352

**15. JavaScript Functions, Objects, and Arrays. . . . . . 353**

JavaScript Functions 353

Defining a Function 353

Returning a Value 356

Returning an Array 358

JavaScript Objects 359

Declaring a Class 359

Creating an Instance 360

Accessing Objects 360

Static Methods and Properties 361

The Legacy Objects Simulated with Functions 361

JavaScript Arrays 363

Arrays 363

Associative Arrays 364

Multidimensional Arrays 365

Using Array Methods 366

Anonymous Functions 372

Arrow Functions 373

Questions 373

**16. JavaScript and PHP Validation and Error Handling. . . . . 375**

Validating User Input with JavaScript 375

The validate.html Document (Part 1) 376

The validate.html Document (Part 2) 379

Regular Expressions 383

Matching Through Metacharacters 383

Wildcard Matching 384

Grouping Through Parentheses 385

Character Classes 386

Indicating a Range 386

Negation 386

Some More Complicated Examples 387

Summary of Metacharacters 389

General Modifiers 391

Using Regular Expressions in JavaScript 391

Using Regular Expressions in PHP 392

Redisplaying a Form After PHP Validation 393

Questions 400

**17. Using Asynchronous Communication. . . . . 403**

The Fetch API 403

Your First Asynchronous Program 404

The Server Half of the Asynchronous Process 406

Cross-Origin Resource Sharing (CORS) 407

Using GET Instead of POST 409

Sending JSON Requests 410

Using XMLHttpRequest 412

Using Frameworks for Asynchronous Communication 413

Questions 413

**18. Advanced CSS. . . . 415**

Attribute Selectors 416

The ^= Operator 417

The \$= Operator 417

The \*= Operator 417

The box-sizing Property 417

CSS Backgrounds 418

The background-clip Property 419

The background-origin Property 421

The background-size Property 421

Using the auto Value 422

Multiple Backgrounds 422

CSS Borders 425

The border-color Property 425

The border-radius Property 426

Box Shadows 428

Element Overflow 429

Multicolumn Layout 429

Colors and Opacity 431

HSL Colors 431

HSLA Colors 432

RGB Colors 432

RGBA Colors 433

The opacity Property 433

Text Effects 433

The text-shadow Property 433

The text-overflow Property 434

The word-wrap Property 435

Web Fonts 435

Google Web Fonts 436

Transformations 438

Transitions 440

Properties to Transition 440

Transition Duration 441

Transition Delay 441

Transition Timing 441

Shorthand Syntax 442

Flexbox 444

Flex Items 445

Flow Direction 445

Justifying Content 447

Aligning Items 449

Aligning Content 450

Resizing Items 451

Flex Wrap 451

Order 453

Item Gaps 453

CSS Grid 454

Grid Container 454

Grid Columns and Rows 455

Grid Flow 456

Placing Grid Items 457

Grid Gaps 458

Alignment 459

Questions 460

**19. Accessing CSS from JavaScript. . . . . . 463**

Revisiting the getElementById Function 463

The byId Function 464

The style Function 464

The by Function 465

Including the Functions 465

Accessing CSS Properties from JavaScript 466

Some Common Properties 466

Other Properties 468

Inline JavaScript 469

The this Keyword 470

Attaching Events to Objects in a Script 470

Attaching to Other Events 471

Adding New Elements 472

Removing Elements 474

Alternatives to Adding and Removing Elements 474

Time-based Events 475

Using setTimeout 475

Using setInterval 476

Using Time-Based Events for Animation 478

Questions 480

**20. Introduction to React. . . . 483**

What Is the Point of React Anyway? 484

Accessing the React Files 485

Including babel.js 486

Our First React Project 487

Using a Class Instead of a Function 488

Pure and Impure Code: A Golden Rule 489

Using Both a Class and a Function 490

Props and Components 490

The Differences Between Using a Class and a Function 492

React State and Life Cycle 492

Events in React 495

Inline JSX Conditional Statements 497

Using Lists and Keys 498

Unique Keys 499

Handling Forms 501

Using Text Input 501

Using textarea 503

Using select 504

React Native 506

Questions 506

**21. Introduction to Node.js. . . . . . . . . 509**

Installing Node.js on Windows 510

Installing Node.js on macOS 516

Installing Node.js on Linux 519

Getting Started with Node.js 520

Building a Functioning Web Server 522

Working with Modules 525

Built-in Modules 526

Installing Modules with npm 526

Accessing MySQL 527

Further Information 529

Questions 530

**22. Bringing It All Together. . . . . . . 531**

Designing a Social Networking App 532

Online Repository 532

functions.php 532

header.php 535

setup.php 537

index.php 539

signup.php 540

Checking for Username Availability 541

Logging In 541

checkuser.php 543

login.php 544

profile.php 547

Adding the “About Me” Text 547

Adding a Profile Image 547

Processing the Image 548

Displaying the Current Profile 548  
members.php 551  
Viewing a User’s Profile 552  
Adding and Dropping Friends 552  
Listing All Members 552  
friends.php 555  
messages.php 558  
logout.php 562  
styles.css 562  
javascript.js 566  
Questions 566

**A. Solutions to the Chapter Questions. . . . . . 567**

**Index. . . . 587**