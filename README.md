# FIFO Page Replacement Algorithm - Web Application
An interactive web-based visualization tool for demonstrating the **FIFO (First-In-First-Out) Page Replacement Algorithm** used in operating systems memory management.
## 🌟 Features
- **Interactive Visualization**: Real-time display of page frames with color-coded pages
- **Live Statistics**: Track page faults and page hits as you add page references
- **User-Friendly Interface**: Simple input fields with visual feedback and smooth animations
- **Responsive Design**: Works seamlessly on desktop, tablet, and mobile devices
- **Educational Tool**: Perfect for students learning about OS memory management concepts
## 📖 What is FIFO Page Replacement?
FIFO (First-In-First-Out) is a simple page replacement algorithm used in operating systems. When a page fault occurs and memory is full, the oldest page (the one that arrived first) is replaced with the new page.
**Key Concepts:**
- **Page Fault**: Occurs when a requested page is not in memory
- **Page Hit**: Occurs when a requested page is already in memory
- **FIFO Queue**: Pages are maintained in order of arrival, and the oldest is removed first
## 🛠️ Technology Stack
- **Frontend**: HTML5, CSS3, JavaScript (ES6+)
- **Libraries**: jQuery, Google Fonts
- **Hosting**: Firebase Hosting
- **Version Control**: Git/GitHub
## 📦 Installation & Setup
### Prerequisites
- Node.js and npm (for Firebase CLI)
- Git
### Local Development
1. **Clone the repository**
   ```bash
   git clone https://github.com/sivakanth1/Page_Replacement_FIFO-Web-Application.git
   cd Page_Replacement_FIFO-Web-Application
   ```
2. **Open the application**
   
   Simply open `public/index.html` in your web browser, or use a local server:
   
   ```bash
   # Using Python 3
   cd public
   python -m http.server 8000
   
   # Using Node.js http-server
   npx http-server public -p 8000
   ```
3. **Access the application**
   
   Navigate to `http://localhost:8000` in your browser
### Firebase Deployment
1. **Install Firebase CLI**
   ```bash
   npm install -g firebase-tools
   ```
2. **Login to Firebase**
   ```bash
   firebase login
   ```
3. **Deploy to Firebase Hosting**
   ```bash
   firebase deploy
   ```
## 📱 Usage
1. **Set Cache Capacity**: Enter the number of page frames available in memory (e.g., 3)
2. **Add Page References**: Enter page numbers one at a time and click "Add"
3. **View Results**: 
   - See the current state of page frames with color-coded visualization
   - Track total page faults and page hits in real-time
4. **Observe FIFO Behavior**: Notice how the oldest page is replaced when memory is full
### Example Walkthrough
```
Capacity: 3
Page Reference String: 1, 2, 3, 4, 1, 2, 5
Step 1: Add 1 → [1, -, -] → Page Fault
Step 2: Add 2 → [1, 2, -] → Page Fault
Step 3: Add 3 → [1, 2, 3] → Page Fault
Step 4: Add 4 → [4, 2, 3] → Page Fault (1 replaced)
Step 5: Add 1 → [4, 1, 3] → Page Fault (2 replaced)
Step 6: Add 2 → [4, 1, 2] → Page Fault (3 replaced)
Step 7: Add 5 → [5, 1, 2] → Page Fault (4 replaced)
Total Page Faults: 7
Total Page Hits: 0
```
## 🎨 Features in Detail
### Visual Design
- **Color-Coded Pages**: Each page frame has a unique vibrant color for easy identification
- **Smooth Animations**: Typewriter effect on headers and smooth transitions
- **Modern UI**: Clean, minimalist design with rounded corners and shadows
- **Focus Effects**: Input fields glow blue when focused
### Algorithm Implementation
- Uses JavaScript `Set` for O(1) page lookup
- Maintains insertion order with array tracking
- Efficiently handles page replacement logic
- Real-time statistics calculation
## 🗂️ Project Structure
```
Page_Replacement_FIFO-Web-Application/
├── public/
│   ├── index.html      # Main HTML file
│   ├── style.css       # Styling and animations
│   ├── script.js       # FIFO algorithm implementation
│   └── 404.html        # Custom 404 error page
├── .firebaserc         # Firebase project config
├── firebase.json       # Firebase hosting config
├── .gitignore          # Git ignore rules
└── README.md           # This file
```
## 🧮 Algorithm Details
The FIFO algorithm implementation follows these steps:
1. **Check Capacity**: If memory has space, add the new page directly
2. **Check Existence**: If page already exists, count it as a hit
3. **Replace Page**: When memory is full:
   - Remove the oldest page (first-in)
   - Add the new page to the queue
   - Increment page fault counter
4. **Update Display**: Refresh the visualization with current state
## 🤝 Contributing
Contributions are welcome! Here's how you can help:
1. Fork the repository
2. Create a feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request
### Ideas for Contributions
- Add reset/clear functionality
- Implement other algorithms (LRU, Optimal)
- Add step-by-step animation mode
- Improve mobile responsiveness
- Add unit tests
- Enhance accessibility (ARIA labels, keyboard navigation)
## 🐛 Known Issues
- jQuery dependency is used but needs to be explicitly loaded
- No input validation for edge cases
- No reset button to clear simulation
## 📝 Future Enhancements
- [ ] Add comparison with LRU and Optimal algorithms
- [ ] Export results as CSV or PDF
- [ ] Step-by-step playback with animation
- [ ] Visual highlighting of page being replaced
- [ ] Algorithm explanation tooltips
- [ ] Dark mode toggle
- [ ] Performance metrics and charts
## 📄 License
This project is open source and available under the [MIT License](LICENSE).
## 👨‍💼 Author
**Sivakanth**
- GitHub: [@sivakanth1](https://github.com/sivakanth1)
## 🙏 Acknowledgments
- Inspired by operating system concepts taught in computer science courses
- Built as an educational tool for students learning about memory management
- Thanks to the open-source community for guidance and resources
## 📚 Resources
- [Operating System Concepts](https://www.os-book.com/) - Silberschatz, Galvin, and Gagne
- [Page Replacement Algorithms](https://en.wikipedia.org/wiki/Page_replacement_algorithm) - Wikipedia
- [Firebase Hosting Documentation](https://firebase.google.com/docs/hosting)
---
**⭐ If you find this project helpful, please consider giving it a star!**
---
*Made with ❤️ for students learning Operating Systems*
