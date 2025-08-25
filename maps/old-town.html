// ==============================================  
// Global Variables and Configuration  
// ==============================================  
const MapSystem = {  
    // Currently active popup  
    activePopup: null,  
    
    // Map data storage  
    locationData: {},  
    
    // Animation settings  
    animationSettings: {  
        popupDuration: 300,  
        hoverDelay: 100,  
        fadeSpeed: 200  
    },  
    
    // Initialize system  
    init: function() {  
        console.log('Map System Initializing...');  
        this.setupEventListeners();  
        this.loadLocationData();  
        this.addNavigationEffects();  
        this.initializeMapInteractions();  
    },  
    
    // Setup event listeners  
    setupEventListeners: function() {  
        // ESC key closes popup  
        document.addEventListener('keydown', (e) => {  
            if (e.key === 'Escape') {  
                this.closeInfo();  
            }  
        });  
        
        // Click overlay to close popup  
        const overlay = document.querySelector('.overlay');  
        if (overlay) {  
            overlay.addEventListener('click', () => this.closeInfo());  
        }  
        
        // Close button  
        const closeBtn = document.querySelector('.close-btn');  
        if (closeBtn) {  
            closeBtn.addEventListener('click', () => this.closeInfo());  
        }  
        
        // Window resize handler  
        window.addEventListener('resize', this.handleResize.bind(this));  
    },  
    
    // Load location data  
    loadLocationData: function() {  
        this.locationData = {  
            // Old Town Data  
            'old-town': {  
                park: {  
                    title: "🌳 Central Public Park",  
                    content: `  
                        <h4>Location & Environment</h4>  
                        <p>The park occupies the largest block in the old town center, surrounded by residential streets on three sides and facing the main commercial avenue on the fourth. Mature maple and oak trees line the paths, with a small artificial lake positioned off-center.</p>  
                        
                        <h4>Special Features</h4>  
                        <ul>  
                            <li><strong>Artificial Lake:</strong> Small pond with weathered wooden dock</li>  
                            <li><strong>Pathways:</strong> Worn concrete walkways with some original cobblestone</li>  
                            <li><strong>Seating:</strong> Green-painted metal park benches and picnic tables</li>  
                            <li><strong>Playground:</strong> Swings, slides, and climbing frames</li>  
                            <li><strong>Lighting:</strong> Tall park lamp posts with frosted globe shades</li>  
                        </ul>  
                        
                        <h4>Daily Activities</h4>  
                        <p>Morning joggers, families with children, elderly chess players, and evening dog walkers frequent this peaceful green space.</p>  
                    `  
                },  
                aria: {  
                    title: "🏠 Aria's Apartment Building",  
                    content: `  
                        <h4>Location & Environment</h4>  
                        <p>Located in a modest small rental apartment building in the quiet residential area. While not particularly comfortable, it's affordable. Aria chose this location for its proximity to the metro and low rent.</p>  
                        
                        <h4>Building Details</h4>  
                        <ul>  
                            <li><strong>Type:</strong> 3-story walk-up apartment building</li>  
                            <li><strong>Condition:</strong> Older construction with basic amenities</li>  
                            <li><strong>Features:</strong> Shared laundry in basement, street parking</li>  
                            <li><strong>Neighborhood:</strong> Quiet residential with tree-lined streets</li>  
                        </ul>  
                        
                        <h4>Resident Profile</h4>  
                        <p>Aria lives here as a budget-conscious choice, prioritizing location over luxury. The building houses young professionals and students.</p>  
                    `  
                },  
                coffee: {  
                    title: "☕ Brew & Books Cafe",  
                    content: `  
                        <h4>Atmosphere</h4>  
                        <p>A cozy neighborhood coffee shop with mismatched furniture, local art on the walls, and the aroma of freshly ground beans. Popular with students, remote workers, and book lovers.</p>  
                        
                        <h4>Menu Highlights</h4>  
                        <ul>  
                            <li><strong>Coffee:</strong> Locally roasted single-origin and blends</li>  
                            <li><strong>Pastries:</strong> Fresh croissants, muffins, and scones</li>  
                            <li><strong>Light Meals:</strong> Sandwiches, salads, and soup of the day</li>  
                            <li><strong>Books:</strong> Small selection of used books for sale</li>  
                        </ul>  
                        
                        <h4>Special Features</h4>  
                        <p>Free WiFi, reading nooks, chess boards, and a small stage for acoustic performances on Friday evenings.</p>  
                    `  
                },  
                grocery: {  
                    title: "🛒 Corner Market",  
                    content: `  
                        <h4>Store Profile</h4>  
                        <p>A family-owned neighborhood grocery store that has served the community for over 30 years. Known for personal service and competitive prices on everyday essentials.</p>  
                        
                        <h4>Products & Services</h4>  
                        <ul>  
                            <li><strong>Fresh Produce:</strong> Local vegetables and fruits</li>  
                            <li><strong>Pantry Items:</strong> Canned goods, dry goods, snacks</li>  
                            <li><strong>Dairy & Meat:</strong> Basic selection of fresh items</li>  
                            <li><strong>Services:</strong> Package pickup, lottery tickets, ATM</li>  
                        </ul>  
                        
                        <h4>Community Role</h4>  
                        <p>Serves as a neighborhood hub where residents catch up on local news and events.</p>  
                    `  
                },  
                metro: {  
                    title: "🚇 Old Town Metro Station",  
                    content: `  
                        <h4>Transportation Hub</h4>  
                        <p>A key transit point connecting the historic old town to downtown and other city districts. Built in the 1980s with recent renovations improving accessibility.</p>  
                        
                        <h4>Station Features</h4>  
                        <ul>  
                            <li><strong>Lines:</strong> Blue and Green line intersection</li>  
                            <li><strong>Accessibility:</strong> Elevator access to platform level</li>  
                            <li><strong>Amenities:</strong> Ticket vending, security cameras, information kiosks</li>  
                            <li><strong>Connections:</strong> Bus stops for routes 15, 23, and 41</li>  
                        </ul>  
                        
                        <h4>Operating Hours</h4>  
                        <p>5:30 AM - 12:30 AM daily, with extended weekend service until 2:00 AM.</p>  
                    `  
                },  
                restaurant: {  
                    title: "🍽️ The Heritage Tavern",  
                    content: `  
                        <h4>Restaurant Profile</h4>  
                        <p>An established neighborhood restaurant serving classic American comfort food with a modern twist. Family-friendly atmosphere with a full bar and outdoor seating.</p>  
                        
                        <h4>Cuisine & Specialties</h4>  
                        <ul>  
                            <li><strong>Entrees:</strong> Grilled steaks, roasted chicken, fresh seafood</li>  
                            <li><strong>Signature Dishes:</strong> Heritage burger, braised short ribs</li>  
                            <li><strong>Bar:</strong> Craft cocktails, local beer selection, wine list</li>  
                            <li><strong>Desserts:</strong> House-made pies and seasonal specialties</li>  
                        </ul>  
                        
                        <h4>Dining Experience</h4>  
                        <p>Warm wood interior, friendly service, and consistent quality have made this a neighborhood favorite for over 15 years.</p>  
                    `  
                }  
            },  
            
            // Downtown Data  
            'downtown': {  
                office: {  
                    title: "🏢 Corporate Tower",  
                    content: `  
                        <h4>Building Profile</h4>  
                        <p>A 25-story modern office building housing various businesses, from startups to established corporations. Features state-of-the-art facilities and sustainable design elements.</p>  
                        
                        <h4>Tenants & Services</h4>  
                        <ul>  
                            <li><strong>Floors 1-5:</strong> Retail and banking services</li>  
                            <li><strong>Floors 6-15:</strong> Mid-size companies and professional services</li>  
                            <li><strong>Floors 16-25:</strong> Corporate headquarters and executive suites</li>  
                            <li><strong>Amenities:</strong> Conference center, fitness facility, parking garage</li>  
                        </ul>  
                    `  
                },  
                mall: {  
                    title: "🛍️ Downtown Shopping Center",  
                    content: `  
                        <h4>Shopping Destination</h4>  
                        <p>A multi-level shopping center with over 150 stores, restaurants, and entertainment venues. The anchor of downtown's retail district.</p>  
                        
                        <h4>Store Categories</h4>  
                        <ul>  
                            <li><strong>Department Stores:</strong> Major retail chains and boutiques</li>  
                            <li><strong>Dining:</strong> Food court plus full-service restaurants</li>  
                            <li><strong>Entertainment:</strong> Movie theater, arcade, bowling</li>  
                            <li><strong>Services:</strong> Banks, phone repair, salon services</li>  
                        </ul>  
                    `  
                },  
                hotel: {  
                    title: "🏨 Grand Plaza Hotel",  
                    content: `  
                        <h4>Luxury Accommodation</h4>  
                        <p>A 4-star business hotel offering premium accommodations and event facilities. Popular with business travelers and tourists exploring the city.</p>  
                        
                        <h4>Hotel Features</h4>  
                        <ul>  
                            <li><strong>Rooms:</strong> 200 guest rooms and suites</li>  
                            <li><strong>Dining:</strong> Fine dining restaurant and lobby bar</li>  
                            <li><strong>Facilities:</strong> Pool, spa, business center, ballroom</li>  
                            <li><strong>Location:</strong> Walking distance to major attractions</li>  
                        </ul>  
                    `  
                }  
            },  
            
            // Suburbs Data  
            'suburbs': {  
                school: {  
                    title: "🏫 Meadowbrook Elementary",  
                    content: `  
                        <h4>Educational Institution</h4>  
                        <p>A well-regarded public elementary school serving grades K-5. Known for its innovative teaching methods and strong community involvement.</p>  
                        
                        <h4>School Features</h4>  
                        <ul>  
                            <li><strong>Programs:</strong> STEM focus, arts integration, ESL support</li>  
                            <li><strong>Facilities:</strong> Computer lab, library, gymnasium, playground</li>  
                            <li><strong>Community:</strong> Active PTA, volunteer programs</li>  
                            <li><strong>Enrollment:</strong> Approximately 400 students</li>  
                        </ul>  
                    `  
                },  
                house: {  
                    title: "🏡 Residential Neighborhood",  
                    content: `  
                        <h4>Community Profile</h4>  
                        <p>A quiet suburban neighborhood with single-family homes, tree-lined streets, and well-maintained properties. Popular with families and professionals.</p>  
                        
                        <h4>Neighborhood Features</h4>  
                        <ul>  
                            <li><strong>Housing:</strong> Mix of ranch and two-story homes</li>  
                            <li><strong>Amenities:</strong> Sidewalks, street lighting, underground utilities</li>  
                            <li><strong>Community:</strong> Neighborhood watch, annual block parties</li>  
                            <li><strong>Transportation:</strong> Bus routes to downtown and metro</li>  
                        </ul>  
                    `  
                }  
            }  
        };  
    },  
    
    // Add navigation page effects  
    addNavigationEffects: function() {  
        // Add parallax effect to navigation cards  
        const mapCards = document.querySelectorAll('.map-card');  
        mapCards.forEach(card => {  
            card.addEventListener('mousemove', (e) => {  
                const rect = card.getBoundingClientRect();  
                const x = e.clientX - rect.left;  
                const y = e.clientY - rect.top;  
                
                const centerX = rect.width / 2;  
                const centerY = rect.height / 2;  
                
                const rotateX = (y - centerY) / 10;  
                const rotateY = (centerX - x) / 10;  
                
                card.style.transform = `perspective(1000px) rotateX(${rotateX}deg) rotateY(${rotateY}deg) translateY(-10px)`;  
            });  
            
            card.addEventListener('mouseleave', () => {  
                card.style.transform = 'perspective(1000px) rotateX(0) rotateY(0) translateY(0)';  
            });  
        });  
        
        // Add typing effect to title  
        this.addTypingEffect();  
    },  
    
    // Initialize map interactions  
    initializeMapInteractions: function() {  
        // Add click events to all location elements  
        const locations = document.querySelectorAll('.location[data-location]');  
        locations.forEach(location => {  
            location.addEventListener('click', (e) => {  
                e.preventDefault();  
                const locationId = location.getAttribute('data-location');  
                const mapType = this.getCurrentMapType();  
                this.showInfo(locationId, mapType);  
            });  
            
            // Add hover effects  
            location.addEventListener('mouseenter', () => {  
                this.addHoverEffect(location);  
            });  
            
            location.addEventListener('mouseleave', () => {  
                this.removeHoverEffect(location);  
            });  
        });  
        
        // Add legend interactions  
        this.initializeLegend();  
    },  
    
    // Get current map type from page  
    getCurrentMapType: function() {  
        const path = window.location.pathname;  
        if (path.includes('old-town')) return 'old-town';  
        if (path.includes('downtown')) return 'downtown';  
        if (path.includes('suburbs')) return 'suburbs';  
        return 'old-town'; // default  
    },  
    
    // Create popup elements if they don't exist
    createPopupElements: function() {
        // Check if overlay exists
        if (!document.querySelector('.overlay')) {
            const overlay = document.createElement('div');
            overlay.className = 'overlay';
            document.body.appendChild(overlay);
            
            // Add click event to close popup
            overlay.addEventListener('click', () => this.closeInfo());
        }
        
        // Check if popup exists
        if (!document.querySelector('.info-popup')) {
            const popup = document.createElement('div');
            popup.className = 'info-popup';
            document.body.appendChild(popup);
        }
    },
    
    // Show location information popup  
    showInfo: function(locationId, mapType) {  
        const locationData = this.locationData[mapType] && this.locationData[mapType][locationId];  
        
        if (!locationData) {  
            console.warn(`No data found for location: ${locationId} in map: ${mapType}`);  
            return;  
        }  
        
        // Create popup if it doesn't exist  
        this.createPopupElements();  
        
        // Update popup content  
        const popup = document.querySelector('.info-popup');  
        const overlay = document.querySelector('.overlay');  
        
        popup.innerHTML = `  
            <button class="close-btn" onclick="MapSystem.closeInfo()">×</button>  
            <div class="popup-header">  
                <h3>${locationData.title}</h3>  
            </div>  
            <div class="popup-content">  
                ${locationData.content}  
            </div>  
        `;  
        
        // Show popup with animation  
        overlay.classList.add('active');  
        popup.classList.add('active');  
        
        this.activePopup = popup;  
        
        // Prevent body scrolling  
        document.body.style.overflow = 'hidden';  
    },  
    
    // Close information popup  
    closeInfo: function() {  
        const popup = document.querySelector('.info-popup');  
        const overlay = document.querySelector('.overlay');  
        
        if (popup && overlay) {  
            popup.classList.remove('active');  
            overlay.classList.remove('active');  
        }  
        
        this.activePopup = null;  
        
        // Restore body scrolling
        document.body.style.overflow = '';
    },
    
    // Add hover effect to location elements
    addHoverEffect: function(element) {
        element.style.transform = 'scale(1.1)';
        element.style.zIndex = '10';
        element.style.filter = 'brightness(1.2)';
        element.style.transition = `all ${this.animationSettings.hoverDelay}ms ease`;
        
        // Add glow effect
        element.style.boxShadow = '0 0 20px rgba(255, 255, 255, 0.6)';
    },
    
    // Remove hover effect from location elements
    removeHoverEffect: function(element) {
        element.style.transform = 'scale(1)';
        element.style.zIndex = '';
        element.style.filter = '';
        element.style.boxShadow = '';
    },
    
    // Handle window resize
    handleResize: function() {
        if (this.activePopup) {
            // Reposition popup if needed
            const popup = document.querySelector('.info-popup');
            if (popup) {
                // Center the popup
                const rect = popup.getBoundingClientRect();
                if (rect.height > window.innerHeight * 0.9) {
                    popup.style.height = '90vh';
                    popup.style.overflowY = 'auto';
                }
            }
        }
    },
    
    // Add typing effect to title
    addTypingEffect: function() {
        const title = document.querySelector('.typing-effect');
        if (!title) return;
        
        const text = title.textContent;
        title.textContent = '';
        title.style.visibility = 'visible';
        
        let index = 0;
        const typeWriter = () => {
            if (index < text.length) {
                title.textContent += text.charAt(index);
                index++;
                setTimeout(typeWriter, 100);
            } else {
                // Add blinking cursor
                title.innerHTML += '<span class="cursor">|</span>';
            }
        };
        
        setTimeout(typeWriter, 500);
    },
    
    // Initialize legend interactions
    initializeLegend: function() {
        const legendItems = document.querySelectorAll('.legend-item');
        legendItems.forEach(item => {
            item.addEventListener('click', () => {
                const category = item.getAttribute('data-category');
                this.filterLocationsByCategory(category);
            });
            
            item.addEventListener('mouseenter', () => {
                const category = item.getAttribute('data-category');
                this.highlightLocationsByCategory(category);
            });
            
            item.addEventListener('mouseleave', () => {
                this.clearHighlights();
            });
        });
    },
    
    // Filter locations by category
    filterLocationsByCategory: function(category) {
        const locations = document.querySelectorAll('.location');
        locations.forEach(location => {
            const locationCategory = location.getAttribute('data-category');
            if (category === 'all' || locationCategory === category) {
                location.style.display = 'block';
                location.style.opacity = '1';
            } else {
                location.style.opacity = '0.3';
            }
        });
    },
    
    // Highlight locations by category
    highlightLocationsByCategory: function(category) {
        const locations = document.querySelectorAll('.location');
        locations.forEach(location => {
            const locationCategory = location.getAttribute('data-category');
            if (locationCategory === category) {
                this.addHoverEffect(location);
            }
        });
    },
    
    // Clear all highlights
    clearHighlights: function() {
        const locations = document.querySelectorAll('.location');
        locations.forEach(location => {
            this.removeHoverEffect(location);
            location.style.opacity = '1';
        });
    },
    
    // Utility function to add smooth scrolling
    smoothScrollTo: function(element) {
        if (element) {
            element.scrollIntoView({ 
                behavior: 'smooth', 
                block: 'center' 
            });
        }
    },
    
    // Add loading animation
    showLoading: function() {
        const loader = document.createElement('div');
        loader.className = 'loading-overlay';
        loader.innerHTML = `
            <div class="loading-spinner">
                <div class="spinner"></div>
                <p>Loading map data...</p>
            </div>
        `;
        document.body.appendChild(loader);
    },
    
    // Remove loading animation
    hideLoading: function() {
        const loader = document.querySelector('.loading-overlay');
        if (loader) {
            loader.remove();
        }
    }
};  

// ==============================================  
// Initialize on page load  
// ==============================================  
document.addEventListener('DOMContentLoaded', function() {  
    MapSystem.init();  
});

// ==============================================  
// Export for use in other modules  
// ==============================================  
if (typeof module !== 'undefined' && module.exports) {  
    module.exports = MapSystem;  
}