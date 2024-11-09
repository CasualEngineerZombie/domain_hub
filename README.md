# DomainHub 🌐

Find your next premium domain with advanced analytics and AI-powered suggestions. DomainHub helps domain investors and businesses make data-driven decisions for domain acquisitions.
 

## Tech Stack 🛠️

- **Backend**: Django 5.0+
- **Frontend**: 
  - Flowbite components
  - TailwindCSS 3.3+  

## Prerequisites 📋

- Python 3.10+
- Node.js 18+ 
- Virtual environment tool (venv recommended)

## Installation 🚀

1. Clone the repository:
```bash
git clone https://github.com/CasualEngineerZombie/domain_hub.git
cd domain_hub
```

2. Create and activate virtual environment:
```bash
python -m venv .venv
source .venv/bin/activate  # On Windows: .venv\Scripts\activate
```

3. Install Python dependencies:
```bash
pip install -r requirements.txt
```

4. Install frontend dependencies:
```bash
npm install
```

5. Configure environment variables:
```bash
cp .env
# Edit .env with your configurations
```

6. Initialize the database:
```bash
python manage.py migrate
```

7. Build TailwindCSS:
```bash
npx tailwindcss -i ./static/src/input.css -o ./static/src/output.css --watch
```

8. Start development server:
```bash
python manage.py runserver
```

## Development 💻

### TailwindCSS Configuration

The project uses TailwindCSS with Flowbite. To modify the configuration, edit `tailwind.config.js`:

```javascript
module.exports = {
  content: [
    './templates/**/*.html',
    './static/js/**/*.js',
    './node_modules/flowbite/**/*.js'
  ],
  theme: {
    extend: {
      // Custom theme extensions
    },
  },
  plugins: [
    require('flowbite/plugin')
  ],
}
```

### Project Structure
```
domain_hub/
├── apps/
│   ├── analytics/       # Domain analysis features
│   ├── suggestions/     # AI suggestion engine
│   └── accounts/        # User management
├── static/
│   ├── css/
│   ├── js/
│   └── images/
├── templates/
├── domain_hub/         # Project settings
└── manage.py
```

## Testing 🧪

Run the test suite:
```bash
python manage.py test
```

For frontend tests:
```bash
npm test
```

## Deployment 🚀

1. Set DEBUG=False in settings
2. Configure your production database
3. Collect static files:
```bash
python manage.py collectstatic
```
4. Set up your web server (Nginx/Apache)
5. Configure SSL certificate
 