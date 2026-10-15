# Site Manager

## Project Overview

The "Site Manager" is a web-based platform designed to significantly enhance efficiency, communication, and productivity on construction sites. In an industry increasingly reliant on technology, this solution streamlines daily operations by providing a centralized hub for site managers, workers, and project managers to interact, manage tasks, and access critical documents. It addresses common challenges such as miscommunication, document loss, and delays, aiming to foster a more organized, productive, and environmentally friendly working environment.

## Features

The platform offers a comprehensive suite of functionalities to optimize construction site management:

* **Website Development:** Built using Django, serving as the core communication and collaboration platform.
* **Task-based Communication:** Comments and tickets on each task, so workers, engineers and supervisors can raise issues and respond.
* **Document Management:** Allows for secure upload and storage of important construction documents, reducing reliance on physical copies.
* **Task Progress Tracking:** Start and end times per task, with progress bars and an overview of completed tasks.
* **Cloud-based Storage:** Utilizes cloud solutions (hosted on AWS EC2) for secure and accessible storage of all project data.
* **Mobile Accessibility:** Designed to be easily accessible via smartphones for convenience on-site.
* **User Authentication:** Secure login and registration for different user roles (workers, companies, admins/engineers).
* **Task Management:** Creation, editing, deletion, and archiving of tasks with estimated timeframes and progression tracking.
* **Location-based Task Information:** Integration of geodata and mapping to specify task locations on detailed construction plans.
* **Team Management:** Assigning tasks to specific teams and monitoring their progress.
* **Data Management:** Functionality to add, show, update, and delete site, location, task, and team data.

## Technologies Used

* **Backend Framework:** Django (Python-based web framework)
* **Programming Language:** Python
* **Database:** SQLite3 (default Django database, designed for scalability to cloud/server)
* **Frontend:** HTML, CSS (with Bootstrap for styling)
* **Deployment:** Amazon Web Services (AWS EC2) for hosting on a Cent OS server, custom domain (`ddp.ink`).
* **Version Control:** Git


## Concept & Workflow

The "Site Manager" features a minimalistic interface designed for clarity and efficiency. The workflow includes:
1.  **Login Screen:** Secure access for workers, companies, and administrators.
2.  **Construction Sites Selection:** Users choose between different construction sites, with optional geodata integration for location overview.
3.  **Task Overview:** Displays daily tasks with estimated timeframes and progress bars. Admins can manage tasks (add, edit, delete, archive, export).
4.  **Task Information:** Provides detailed task location on construction plans, a comment section for issues, and serves as the start/endpoint for tasks.

## How to Run Locally

1. Clone the repository and create a virtual environment:
    ```bash
    git clone <this-repo-url>
    cd Site-Manager
    python -m venv venv
    venv\Scripts\activate          # Windows
    # source venv/bin/activate     # macOS/Linux
    ```

2. Install the dependencies:
    ```bash
    pip install -r requirements.txt
    ```

3. Set up the database and an admin account:
    ```bash
    cd construction_management
    python manage.py makemigrations
    python manage.py migrate
    python manage.py createsuperuser
    ```

4. Run the development server and open `http://127.0.0.1:8000/`:
    ```bash
    python manage.py runserver
    ```

For deployment, set the environment variables `DJANGO_SECRET_KEY`, `DJANGO_DEBUG=False` and `DJANGO_ALLOWED_HOSTS` instead of using the development defaults.

## Future Outlook

The project is a strong foundational layer, with plans for further expansion. Future features aim to include:
* Automatic data upload for tasks and locations via files.
* Integrated map on webpage for precise task location pinning.
* Advanced features like progress bars and Gantt charts for administrators.
* Automated hierarchy building for new construction sites.

