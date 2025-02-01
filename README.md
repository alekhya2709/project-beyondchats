
# User Registration & Chatbot Integration - Web Application

This project covers the complete user registration process, organization setup, and chatbot integration, along with a user interface to manage the setup flow. It includes features such as email verification, scraping a company’s website for chatbot training, and integration of a dummy chatbot on the user’s website.

## Features

1. **User Registration**:
   - Users can register by entering their name, email, and password.
   - Users can also choose to register via Google.
   - An email verification code is required to ensure legitimate user registrations.

2. **Setup Organization**:
   - Users input their company name, website URL, and a description.
   - The company’s website URL is used to auto-fetch the meta-description for the company (bonus feature).
   - Dummy data is used for auto-fetching and scraping the website's pages.
   - A UI displays a list of webpages that have been detected, scraped, and are pending.
   - Users can click on any webpage to view the chunks of data scraped from the page.
   - Users can either wait for chatbot training to finish or move to the next section.

3. **Chatbot Integration & Testing**:
   - **Test Chatbot Button**: Opens a client's website with a dummy chatbot integration.
     - A topbar informs users if the chatbot is not working and provides an option to give feedback.
   - **Integrate on Your Website**:
     - Provides easy-to-follow instructions for copying and pasting a dummy code into the `<head>` of their website.
     - Option to email instructions to the client’s developer.
   - **Test Integration**: Opens a new screen showing a SUCCESS UI with confetti or another celebratory animation.
     - Following successful integration, users are shown:
       - "Explore Admin Panel" button.
       - "Start talking to your chatbot" button.
       - Social media sharing buttons.

4. **UI for Pending Web Scraping**:
   - A section that displays scraped webpages with statuses (pending, scraped, etc.).
   - The user can click on each page to see the data chunks extracted from the page.

5. **Fallback UI**:
   - If the integration cannot be detected successfully, a different UI is shown with instructions for troubleshooting.

## Table of Contents
- [Installation](#installation)
- [Usage](#usage)
- [Features](#features)
- [Technologies Used](#technologies-used)
- [Customization](#customization)
- [Contributing](#contributing)
- [License](#license)

## Installation

To get started with this project locally:

1. **Clone the repository**:
   ```bash
   git clone https://github.com/yourusername/chatbot-integration.git
   ```

2. **Navigate into the project folder**:
   ```bash
   cd chatbot-integration
   ```

3. **Install dependencies**:
   ```bash
   npm install
   ```

4. **Start the development server**:
   ```bash
   npm start
   ```

Now, the application will be available at `http://localhost:3000/`.

## Usage

- The app consists of several sections:
  - **User Registration**: A form for users to register with email/password or Google.
  - **Organization Setup**: A form where users input company details, and the system auto-fetches metadata from their website.
  - **Chatbot Integration & Testing**: Provides buttons for testing and integrating the chatbot on the user’s website.
  - **Pending Web Scraping**: Displays webpages and scraped content for training the chatbot.

### Example usage:
1. **User Registration**:
   - Enter name, email, and password, or use Google registration.
   - A verification email will be sent to the user’s email for validation.

2. **Setup Organization**:
   - Enter company name, website URL, and description.
   - The app will show scraped webpage data with statuses like “Pending” or “Scraped.”

3. **Chatbot Integration**:
   - Click on “Test Chatbot” to simulate the chatbot on the client’s website.
   - Choose “Integrate on your website” to get integration code or send it to a developer.
   - If successful, a "Success" UI with confetti appears along with buttons to explore the admin panel and interact with the chatbot.

## Features

- **User Registration with Email Verification**: 
  Users register by filling out their name, email, and password. An email verification step ensures genuine signups.
  
- **Auto-Scraping**: 
  The application scrapes the company website in the background and displays a list of detected webpages with their scraping status (scraped or pending).

- **Chatbot Integration**: 
  The user can test the chatbot integration on their website or follow integration instructions.

- **Success UI**: 
  After successful integration, a fun UI with confetti is shown to congratulate the user. 

- **Fallback UI**: 
  If integration is not successful, a fallback UI is displayed with instructions on troubleshooting.

## Technologies Used
- **React**: JavaScript library for building user interfaces.
- **CSS**: Styling for the components.
- **Node.js**: Backend server (assumed) for scraping the website content and providing data.
- **Email Service**: For sending verification codes to users.

## Customization

To customize this project:
- **Registration Form**: Modify the fields for additional user information.
- **Website Scraping**: Change the website scraping logic (if necessary).
- **Chatbot UI**: You can swap out the dummy chatbot integration for an actual service.

### Example of changing registration form fields:
You can update the `RegistrationForm` component to add more fields or validations as needed.

```javascript
// Add additional fields in RegistrationForm.js
<form>
  <input type="text" placeholder="Full Name" required />
  <input type="email" placeholder="Email" required />
  <input type="password" placeholder="Password" required />
  <input type="text" placeholder="Phone Number" />
  <button type="submit">Register</button>
</form>
```

### Modifying Scraping Logic:
In the backend server, the scraping logic can be modified to scrape more specific data from the website. You may need to change the scraping function to look for different meta tags or data structures.

## Contributing

If you'd like to contribute to this project:

1. Fork the repository.
2. Create a new branch (`git checkout -b feature-branch`).
3. Make your changes.
4. Commit your changes (`git commit -am 'Add new feature'`).
5. Push to the branch (`git push origin feature-branch`).
6. Create a pull request.

## License

This project is open-source and available under the MIT License.
