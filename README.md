# CSS Layouts and Responsive Design

## Objectives

Implement Flexbox and Grid for layout design.
Make the webpage responsive using media queries.
Ensure proper alignment and spacing.

## Instructions

- use Flexbox or CSS Grid.
- Add a navigation bar and structure the content.
- Use media queries to adjust layout for mobile, tablet, and desktop.

>[!NOTE]
>  - Include at least:
>  - navigation bar
>  - media queries

# Tasks

- Apply Flexbox or Grid for layout.
- Make the page responsive.
- Test across different screen sizes.

Happy Coding! 💻✨

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Responsive Layout with Flexbox and Grid</title>
    <style>
        /* Basic reset */
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        /* Body and layout container */
        body {
            font-family: Arial, sans-serif;
            line-height: 1.6;
        }

        /* Navigation Bar */
        nav {
            background-color: #333;
            padding: 1rem;
        }

        nav ul {
            display: flex;
            justify-content: space-around;
            list-style: none;
        }

        nav ul li {
            margin: 0 1rem;
        }

        nav ul li a {
            color: white;
            text-decoration: none;
            font-weight: bold;
        }

        /* Main content area */
        .container {
            display: grid;
            grid-template-columns: 1fr 3fr; /* Two columns: 1fr for sidebar, 3fr for main content */
            gap: 2rem;
            padding: 2rem;
        }

        .sidebar {
            background-color: #f4f4f4;
            padding: 1rem;
        }

        .main-content {
            background-color: #fff;
            padding: 1rem;
            box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
        }

        /* Footer */
        footer {
            text-align: center;
            padding: 1rem;
            background-color: #333;
            color: white;
        }

        /* Media Queries for responsiveness */
        @media (max-width: 768px) {
            /* For tablets */
            nav ul {
                flex-direction: column;
                align-items: center;
            }

            .container {
                grid-template-columns: 1fr; /* Stack content vertically on small screens */
            }
        }

        @media (max-width: 480px) {
            /* For mobile devices */
            .container {
                grid-template-columns: 1fr;
                padding: 1rem;
            }

            .sidebar {
                display: none; /* Hide sidebar on mobile */
            }
        }
    </style>
</head>
<body>

    <!-- Navigation Bar -->
    <nav>
        <ul>
            <li><a href="#">Home</a></li>
            <li><a href="#">About</a></li>
            <li><a href="#">Services</a></li>
            <li><a href="#">Contact</a></li>
        </ul>
    </nav>

    <!-- Main Content -->
    <div class="container">
        <!-- Sidebar -->
        <div class="sidebar">
            <h3>Sidebar</h3>
            <p>This is the sidebar content.</p>
        </div>

        <!-- Main Content Area -->
        <div class="main-content">
            <h1>Welcome to the Website</h1>
            <p>This is the main content area. Resize the window to see how the layout adjusts to different screen sizes.</p>
        </div>
    </div>

    <!-- Footer -->
    <footer>
        <p>&copy; 2025 Your Website. All Rights Reserved.</p>
    </footer>

</body>
</html>

