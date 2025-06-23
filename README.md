# 📝 Laravel Livewire Task Manager

A modern, responsive task management application built with Laravel 10, Livewire 3, and Bootstrap 5. Perfect for learning modern Laravel development or managing your daily tasks efficiently.

![Laravel](https://img.shields.io/badge/Laravel-10.x-red?style=flat-square&logo=laravel)
![Livewire](https://img.shields.io/badge/Livewire-3.x-blue?style=flat-square)
![Bootstrap](https://img.shields.io/badge/Bootstrap-5.3-purple?style=flat-square&logo=bootstrap)
![PHP](https://img.shields.io/badge/PHP-8.1+-777BB4?style=flat-square&logo=php)
![License](https://img.shields.io/badge/License-MIT-green?style=flat-square)

## 🚀 Features

### ✨ Core Functionality
- **User Authentication** - Complete registration and login system
- **Task Management** - Create, read, update, and delete tasks
- **Real-time Updates** - Instant UI updates with Livewire
- **Task Organization** - Set status (Pending, In Progress, Completed) and priority levels
- **Due Date Tracking** - Set due dates with overdue alerts
- **Search & Filter** - Find tasks quickly by title, status, or priority

### 🎨 User Interface
- **Responsive Design** - Works perfectly on desktop, tablet, and mobile
- **Bootstrap 5** - Modern, clean, and professional interface
- **Interactive Cards** - Beautiful task cards with hover effects
- **Status Badges** - Color-coded status and priority indicators
- **Dashboard Analytics** - Visual overview of task statistics

### 🔧 Technical Features
- **Laravel Breeze** - Secure authentication system
- **Livewire Components** - No-page-reload interactions
- **Form Validation** - Real-time form validation with error messages
- **Pagination** - Efficient handling of large task lists
- **Database Relations** - Proper user-task relationships
- **SQLite Support** - Easy setup with SQLite or MySQL

## 📱 Screenshots

### Dashboard
> Clean overview of your task statistics and quick actions

### Task Manager
> Complete task management interface with search and filters

### Responsive Design
> Works beautifully on all devices

*Screenshots coming soon - feel free to contribute!*

## 🛠️ Installation

### Prerequisites
- PHP 8.1 or higher
- Composer
- Node.js & NPM
- MySQL or SQLite

### Quick Setup

1. **Clone the Repository**
```bash
git clone https://github.com/yourusername/laravel-livewire-task-manager.git
cd laravel-livewire-task-manager
```

2. **Install Dependencies**
```bash
composer install
npm install
```

3. **Environment Setup**
```bash
cp .env.example .env
php artisan key:generate
```

4. **Database Configuration**

**Option A: SQLite (Recommended for development)**
```bash
touch database/database.sqlite
```
Update `.env`:
```env
DB_CONNECTION=sqlite
```

**Option B: MySQL**
```env
DB_CONNECTION=mysql
DB_HOST=127.0.0.1
DB_PORT=3306
DB_DATABASE=task_manager
DB_USERNAME=root
DB_PASSWORD=your_password
```

5. **Run Migrations**
```bash
php artisan migrate
```

6. **Compile Assets**
```bash
npm run dev
```

7. **Start Development Server**
```bash
php artisan serve
```

8. **Access Application**
Open your browser and visit: `http://localhost:8000`

## 🎯 Usage

### Getting Started
1. **Register** a new account or **login** with existing credentials
2. **Dashboard** - View your task statistics and quick actions
3. **Create Tasks** - Click "Manage Tasks" to start adding tasks
4. **Organize** - Set status, priority, and due dates for better organization
5. **Search & Filter** - Use the powerful search and filtering system to find tasks quickly

### Task Management
- **Create**: Fill out the form and click "Create Task"
- **Edit**: Click the dropdown menu on any task card and select "Edit"
- **Delete**: Use the dropdown menu to delete tasks (with confirmation)
- **Filter**: Use status and priority filters to organize your view
- **Search**: Type in the search box to find specific tasks

### Status Types
- **Pending** - Tasks that haven't been started
- **In Progress** - Tasks currently being worked on
- **Completed** - Finished tasks

### Priority Levels
- **Low** - Green badge
- **Medium** - Yellow badge  
- **High** - Red badge

## 🧰 Technologies Used

### Backend
- **Laravel 10** - PHP web application framework
- **Livewire 3** - Full-stack framework for Laravel
- **Laravel Breeze** - Authentication scaffolding
- **Eloquent ORM** - Database relationships and queries

### Frontend
- **Bootstrap 5** - CSS framework for responsive design
- **Bootstrap Icons** - Comprehensive icon library
- **Blade Templates** - Laravel's templating engine
- **Alpine.js** - (Included with Livewire) for enhanced interactions

### Database
- **SQLite** - Lightweight database (default)
- **MySQL** - Production-ready database option

## 📁 Project Structure

```
├── app/
│   ├── Livewire/
│   │   └── TaskManager.php          # Main Livewire component
│   └── Models/
│       ├── Task.php                 # Task model with relationships
│       └── User.php                 # User model
├── database/
│   └── migrations/                  # Database schema
├── resources/
│   └── views/
│       ├── livewire/
│       │   └── task-manager.blade.php    # Task manager interface
│       ├── layouts/
│       │   └── app.blade.php            # Main layout with Bootstrap
│       └── dashboard.blade.php          # Dashboard with statistics
└── routes/
    └── web.php                      # Application routes
```

## 🔧 Configuration

### Customizing Task Status
Edit `app/Models/Task.php` to modify available status options:
```php
'status' => 'required|in:pending,in_progress,completed,on_hold'
```

### Changing Priority Levels
Update the priority validation and colors in the Task model:
```php
'priority' => 'required|in:low,medium,high,urgent'
```

### Database Switching
To switch from SQLite to MySQL:
1. Update `.env` database settings
2. Run `php artisan migrate:fresh`

## 🚀 Deployment

### Production Setup
1. **Environment**: Set `APP_ENV=production` in `.env`
2. **Database**: Configure production database
3. **Cache**: Run optimization commands
```bash
php artisan config:cache
php artisan route:cache
php artisan view:cache
```

### Hosting Platforms
- **Shared Hosting**: Upload files via FTP/cPanel
- **VPS**: Use traditional LAMP stack
- **Laravel Forge**: Automated deployment
- **Heroku**: Use Heroku PostgreSQL addon

## 🤝 Contributing

We welcome contributions! Here's how you can help:

### Ways to Contribute
- 🐛 Report bugs
- 💡 Suggest new features
- 📝 Improve documentation
- 🎨 Enhance UI/UX
- 🧪 Add tests
- 🌐 Add translations

### Development Setup
1. Fork the repository
2. Create a feature branch: `git checkout -b feature/amazing-feature`
3. Make your changes
4. Add tests if applicable
5. Commit: `git commit -m 'Add amazing feature'`
6. Push: `git push origin feature/amazing-feature`
7. Open a Pull Request

### Coding Standards
- Follow PSR-12 coding standards
- Write descriptive commit messages
- Add comments for complex logic
- Update documentation for new features

## 📋 Roadmap

### Upcoming Features
- [ ] **Categories/Tags** - Organize tasks with custom categories
- [ ] **Team Collaboration** - Share tasks with team members
- [ ] **File Attachments** - Attach files to tasks
- [ ] **Comments System** - Add notes and updates to tasks
- [ ] **Email Notifications** - Get notified about due dates
- [ ] **API Endpoints** - RESTful API for mobile apps
- [ ] **Dark Mode** - Toggle between light and dark themes
- [ ] **Time Tracking** - Track time spent on tasks
- [ ] **Subtasks** - Break down complex tasks
- [ ] **Calendar View** - Visual calendar interface

### Version History
- **v1.0.0** - Initial release with basic task management
- **v1.1.0** - Added search and filtering (Coming Soon)
- **v1.2.0** - Enhanced UI and mobile optimization (Coming Soon)

## 🐛 Known Issues

- Pagination may reset when using filters (minor UX issue)
- Date picker styling could be improved on mobile
- File upload feature is planned but not yet implemented

Report bugs in the [Issues](https://github.com/yourusername/laravel-livewire-task-manager/issues) section.

## 📚 Learning Resources

### For Beginners
- [Laravel Documentation](https://laravel.com/docs)
- [Livewire Documentation](https://livewire.laravel.com/docs)
- [Bootstrap Documentation](https://getbootstrap.com/docs/5.3)

### Tutorials Used
- [Laravel Bootcamp](https://bootcamp.laravel.com/)
- [Livewire Screencast Series](https://laracasts.com/series/livewire)

## 📄 License

This project is open-sourced software licensed under the [MIT license](LICENSE).

```
MIT License

Copyright (c) 2025 [Darbaz Rassul]

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
```

## 👨‍💻 Author

**[Darbaz]**
- GitHub: [@Darbaz Rasull](https://github.com/darbazrasul)
- LinkedIn: [@Darbaz Rasull](https://www.linkedin.com/in/darbaz-rasull-19375a252/)
- Email: darbazrasul721@gmail.com

## 🙏 Acknowledgments

- **Laravel Team** - For the amazing framework
- **Livewire Team** - For making real-time interactions simple
- **Bootstrap Team** - For the excellent CSS framework
- **Community** - For feedback and contributions

## ⭐ Show Your Support

If this project helped you, please consider:
- ⭐ **Starring** the repository
- 🐛 **Reporting** any bugs you find
- 💡 **Suggesting** new features
- 🤝 **Contributing** to the codebase
- 📢 **Sharing** with others who might find it useful

---

**Made with ❤️ for the Laravel community**

*Happy task managing! 🎯*
