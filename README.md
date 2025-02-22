# hugo-mock-landing-page-autodeployed 
Part IV of HW 1: Mock Hugo Landing Page (Autodeployed Version)

A modern and responsive landing page built with Hugo and a customized version of the Hugo Bootstrap Theme. This project showcases features of the StudyBuddy app, including Study Group Matching, Progress Tracking, and more.

Features:

Study Group Matching: Match with peers in your courses for collaborative study sessions.

Study Buddy Forum: Post and answer questions with students in the same courses.

Progress Tracker: Track academic progress and compare it with study group peers.

Group Scheduling: Schedule study sessions easily with built-in tools.

Reminders: Get reminders for upcoming study sessions and tasks.

# Description of workflow 

I used a GitHub Actions workflow that automatically builds and deploys the Hugo site to GitHub Pages whenever changes are pushed to the main branch. The workflow performs the following steps:

1. Checkout Code: The workflow checks out the repository's code, including any submodules (e.g., Hugo themes).

2. Setup Hugo: It installs Hugo version 0.144.1 with extended features.

3. Build Website: The site is built using Hugo, including draft posts (-D), cleaning up unused files (--gc), and minifying the output (--minify).

4. Deploy to GitHub Pages: The built site is deployed to the gh-pages branch, which GitHub Pages uses to serve the site.

The workflow is defined in the .github/workflows/hugo.yml file and uses reusable actions from the GitHub Actions Marketplace, such as actions/checkout, peaceiris/actions-hugo, and peaceiris/actions-gh-pages.

