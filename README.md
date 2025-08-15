# sb3-react-animalduo — Global Pet Product Commerce Platform

## ✍️ Author
- Name: Shiwoo Min
- Role: Full-Stack Developer · DevOps Engineer · Founder of Artiordex  
- Contact: artiordex@gmail.com

## 📝 Overview
AnimalDuo is a comprehensive global pet product commerce platform that combines the power of Spring Boot 3 backend with a modern React frontend. The platform features a modular microservice architecture, comprehensive RESTful APIs, and Hibernate ORM for robust data management. Designed with scalability in mind, AnimalDuo provides a complete e-commerce solution for pet products, including inventory management, order processing, payment integration, and multi-language support for global reach.

## 🚀 Goals
1. Master Spring Boot 3 features including native compilation and improved performance
2. Implement reactive programming with Spring WebFlux for high-throughput operations
3. Build robust data layer using Hibernate 6 with advanced ORM features
4. Create scalable microservice architecture with clean API boundaries
5. Develop modern React frontend with TypeScript and state management
6. Integrate payment gateways and multi-currency support for global commerce
7. Implement comprehensive testing strategies for API testing and integration
8. Design cloud-native architecture ready for containerization and deployment

## ⚙️ Tech Stack

### **Backend**
- **Framework**: Spring Boot 3.2, Spring Security 6
- **Database**: PostgreSQL 15, Hibernate 6.4, JPA
- **Caching**: Redis 7, Spring Cache
- **Message Queue**: RabbitMQ, Spring AMQP
- **API**: Spring WebFlux, RESTful APIs, OpenAPI 3
- **Testing**: JUnit 5, TestContainers, MockMvc
- **IDE**: IntelliJ IDEA Ultimate 2024.x

### **Frontend**
- **Framework**: React 18, TypeScript, Vite
- **State Management**: Redux Toolkit, React Query
- **UI Library**: Material-UI (MUI), Tailwind CSS
- **Routing**: React Router v6
- **Testing**: Jest, React Testing Library
- **IDE**: Visual Studio Code with Extensions

### **DevOps & Infrastructure**
- **Build**: Maven 3.9, Docker, Docker Compose
- **Monitoring**: Spring Actuator, Micrometer, Prometheus
- **Documentation**: Swagger UI, Spring REST Docs
- **JDK**: Java 21 (LTS)

## 🗓 3-Week Development Plan

#### Week 1 - Backend Foundation & Core Architecture
1. Spring Boot 3 project setup with modular structure
2. Database design with Hibernate entities and relationships
3. Core domain services: Product, User, Order management
4. Authentication & authorization with Spring Security
5. RESTful API development with proper HTTP status handling

#### Week 2 - Advanced Backend Features & Integration
6. Payment gateway integration (Stripe, PayPal)
7. File upload system for product images (AWS S3 integration)
8. Caching strategies with Redis for performance optimization
9. Message queuing for order processing and notifications
10. Comprehensive API testing with TestContainers

#### Week 3 - Frontend Development & Deployment
11. React application setup with TypeScript configuration
12. Component library development with Material-UI
13. State management implementation with Redux Toolkit
14. API integration and error handling
15. Responsive design and multi-language support
16. Docker containerization and deployment preparation

## 🗃 Project Structure
```
sb3-react-animalduo/
├─ backend/                           # Spring Boot 3 backend
│  ├─ src/
│  │  ├─ main/
│  │  │  ├─ java/
│  │  │  │  └─ com/
│  │  │  │     └─ artiordex/
│  │  │  │        └─ animalduo/
│  │  │  │           ├─ AnimalDuoApplication.java
│  │  │  │           │
│  │  │  │           ├─ config/          # Configuration classes
│  │  │  │           │  ├─ SecurityConfig.java
│  │  │  │           │  ├─ DatabaseConfig.java
│  │  │  │           │  ├─ RedisConfig.java
│  │  │  │           │  └─ RabbitMQConfig.java
│  │  │  │           │
│  │  │  │           ├─ domain/          # Domain models & entities
│  │  │  │           │  ├─ user/
│  │  │  │           │  │  ├─ User.java
│  │  │  │           │  │  ├─ Role.java
│  │  │  │           │  │  └─ UserAddress.java
│  │  │  │           │  │
│  │  │  │           │  ├─ product/
│  │  │  │           │  │  ├─ Product.java
│  │  │  │           │  │  ├─ Category.java
│  │  │  │           │  │  ├─ Brand.java
│  │  │  │           │  │  └─ ProductImage.java
│  │  │  │           │  │
│  │  │  │           │  ├─ order/
│  │  │  │           │  │  ├─ Order.java
│  │  │  │           │  │  ├─ OrderItem.java
│  │  │  │           │  │  ├─ Payment.java
│  │  │  │           │  │  └─ Shipping.java
│  │  │  │           │  │
│  │  │  │           │  └─ common/
│  │  │  │           │     ├─ BaseEntity.java
│  │  │  │           │     └─ Address.java
│  │  │  │           │
│  │  │  │           ├─ repository/      # JPA repositories
│  │  │  │           │  ├─ UserRepository.java
│  │  │  │           │  ├─ ProductRepository.java
│  │  │  │           │  ├─ OrderRepository.java
│  │  │  │           │  └─ CategoryRepository.java
│  │  │  │           │
│  │  │  │           ├─ service/         # Business logic layer
│  │  │  │           │  ├─ user/
│  │  │  │           │  │  ├─ UserService.java
│  │  │  │           │  │  └─ AuthService.java
│  │  │  │           │  │
│  │  │  │           │  ├─ product/
│  │  │  │           │  │  ├─ ProductService.java
│  │  │  │           │  │  └─ CategoryService.java
│  │  │  │           │  │
│  │  │  │           │  ├─ order/
│  │  │  │           │  │  ├─ OrderService.java
│  │  │  │           │  │  ├─ PaymentService.java
│  │  │  │           │  │  └─ ShippingService.java
│  │  │  │           │  │
│  │  │  │           │  └─ common/
│  │  │  │           │     ├─ FileUploadService.java
│  │  │  │           │     ├─ EmailService.java
│  │  │  │           │     └─ CacheService.java
│  │  │  │           │
│  │  │  │           ├─ controller/      # REST controllers
│  │  │  │           │  ├─ UserController.java
│  │  │  │           │  ├─ ProductController.java
│  │  │  │           │  ├─ OrderController.java
│  │  │  │           │  ├─ PaymentController.java
│  │  │  │           │  └─ AdminController.java
│  │  │  │           │
│  │  │  │           ├─ dto/             # Data Transfer Objects
│  │  │  │           │  ├─ request/
│  │  │  │           │  │  ├─ LoginRequest.java
│  │  │  │           │  │  ├─ ProductCreateRequest.java
│  │  │  │           │  │  └─ OrderCreateRequest.java
│  │  │  │           │  │
│  │  │  │           │  └─ response/
│  │  │  │           │     ├─ UserResponse.java
│  │  │  │           │     ├─ ProductResponse.java
│  │  │  │           │     └─ OrderResponse.java
│  │  │  │           │
│  │  │  │           ├─ exception/       # Exception handling
│  │  │  │           │  ├─ GlobalExceptionHandler.java
│  │  │  │           │  ├─ BusinessException.java
│  │  │  │           │  └─ ResourceNotFoundException.java
│  │  │  │           │
│  │  │  │           ├─ security/        # Security configuration
│  │  │  │           │  ├─ JwtTokenProvider.java
│  │  │  │           │  ├─ JwtAuthenticationFilter.java
│  │  │  │           │  └─ CustomUserDetailsService.java
│  │  │  │           │
│  │  │  │           └─ util/            # Utility classes
│  │  │  │              ├─ DateUtil.java
│  │  │  │              ├─ ValidationUtil.java
│  │  │  │              └─ PasswordEncoder.java
│  │  │  │
│  │  │  └─ resources/
│  │  │     ├─ application.yml         # Main configuration
│  │  │     ├─ application-dev.yml     # Development profile
│  │  │     ├─ application-prod.yml    # Production profile
│  │  │     ├─ db/
│  │  │     │  ├─ migration/           # Flyway migrations
│  │  │     │  │  ├─ V1__Create_user_tables.sql
│  │  │     │  │  ├─ V2__Create_product_tables.sql
│  │  │     │  │  └─ V3__Create_order_tables.sql
│  │  │     │  │
│  │  │     │  └─ data.sql             # Sample data
│  │  │     │
│  │  │     ├─ static/                 # Static resources
│  │  │     └─ templates/              # Email templates
│  │  │
│  │  └─ test/
│  │     ├─ java/
│  │     │  └─ com/artiordex/animalduo/
│  │     │     ├─ integration/         # Integration tests
│  │     │     │  ├─ UserControllerTest.java
│  │     │     │  └─ ProductControllerTest.java
│  │     │     │
│  │     │     ├─ service/             # Service tests
│  │     │     │  ├─ UserServiceTest.java
│  │     │     │  └─ ProductServiceTest.java
│  │     │     │
│  │     │     └─ repository/          # Repository tests
│  │     │        ├─ UserRepositoryTest.java
│  │     │        └─ ProductRepositoryTest.java
│  │     │
│  │     └─ resources/
│  │        ├─ application-test.yml    # Test configuration
│  │        └─ test-data.sql          # Test data
│  │
│  └─ pom.xml                         # Maven configuration
│
├─ frontend/                          # React frontend
│  ├─ public/
│  │  ├─ index.html
│  │  ├─ favicon.ico
│  │  ├─ manifest.json               # PWA manifest
│  │  └─ locales/                    # i18n translation files
│  │     ├─ en/
│  │     │  └─ common.json
│  │     ├─ ko/
│  │     │  └─ common.json
│  │     └─ ja/
│  │        └─ common.json
│  │
│  ├─ src/
│  │  ├─ components/                  # Reusable components
│  │  │  ├─ common/                  # Shared UI components
│  │  │  │  ├─ layout/
│  │  │  │  │  ├─ Header.tsx
│  │  │  │  │  ├─ Footer.tsx
│  │  │  │  │  ├─ Navbar.tsx
│  │  │  │  │  └─ Sidebar.tsx
│  │  │  │  │
│  │  │  │  ├─ ui/                   # Basic UI elements
│  │  │  │  │  ├─ Button.tsx
│  │  │  │  │  ├─ Input.tsx
│  │  │  │  │  ├─ Modal.tsx
│  │  │  │  │  ├─ Loading.tsx
│  │  │  │  │  ├─ ErrorBoundary.tsx
│  │  │  │  │  └─ Pagination.tsx
│  │  │  │  │
│  │  │  │  ├─ forms/                # Form components
│  │  │  │  │  ├─ FormField.tsx
│  │  │  │  │  ├─ SearchBox.tsx
│  │  │  │  │  └─ FileUpload.tsx
│  │  │  │  │
│  │  │  │  └─ feedback/             # User feedback
│  │  │  │     ├─ Toast.tsx
│  │  │  │     ├─ Alert.tsx
│  │  │  │     └─ ConfirmDialog.tsx
│  │  │  │
│  │  │  ├─ product/                 # Product-related components
│  │  │  │  ├─ ProductCard.tsx
│  │  │  │  ├─ ProductDetail.tsx
│  │  │  │  ├─ ProductList.tsx
│  │  │  │  ├─ ProductFilter.tsx
│  │  │  │  ├─ ProductGallery.tsx
│  │  │  │  ├─ ProductReviews.tsx
│  │  │  │  ├─ CategoryNavigation.tsx
│  │  │  │  └─ RecommendedProducts.tsx
│  │  │  │
│  │  │  ├─ cart/                    # Shopping cart components
│  │  │  │  ├─ CartItem.tsx
│  │  │  │  ├─ CartSummary.tsx
│  │  │  │  ├─ CartSidebar.tsx
│  │  │  │  ├─ Checkout.tsx
│  │  │  │  └─ PaymentForm.tsx
│  │  │  │
│  │  │  ├─ user/                    # User management components
│  │  │  │  ├─ auth/
│  │  │  │  │  ├─ Login.tsx
│  │  │  │  │  ├─ Register.tsx
│  │  │  │  │  ├─ ForgotPassword.tsx
│  │  │  │  │  └─ PasswordReset.tsx
│  │  │  │  │
│  │  │  │  ├─ profile/
│  │  │  │  │  ├─ Profile.tsx
│  │  │  │  │  ├─ AddressBook.tsx
│  │  │  │  │  ├─ OrderHistory.tsx
│  │  │  │  │  └─ Wishlist.tsx
│  │  │  │  │
│  │  │  │  └─ dashboard/            # User dashboard
│  │  │  │     ├─ DashboardLayout.tsx
│  │  │  │     ├─ AccountSettings.tsx
│  │  │  │     └─ NotificationSettings.tsx
│  │  │  │
│  │  │  ├─ admin/                   # Admin panel components
│  │  │  │  ├─ AdminLayout.tsx
│  │  │  │  ├─ AdminSidebar.tsx
│  │  │  │  ├─ dashboard/
│  │  │  │  │  ├─ AdminDashboard.tsx
│  │  │  │  │  ├─ SalesChart.tsx
│  │  │  │  │  └─ AnalyticsCard.tsx
│  │  │  │  │
│  │  │  │  ├─ products/
│  │  │  │  │  ├─ ProductManagement.tsx
│  │  │  │  │  ├─ ProductForm.tsx
│  │  │  │  │  └─ CategoryManagement.tsx
│  │  │  │  │
│  │  │  │  ├─ orders/
│  │  │  │  │  ├─ OrderManagement.tsx
│  │  │  │  │  ├─ OrderDetail.tsx
│  │  │  │  │  └─ ShippingTracker.tsx
│  │  │  │  │
│  │  │  │  └─ users/
│  │  │  │     ├─ UserManagement.tsx
│  │  │  │     └─ UserDetail.tsx
│  │  │  │
│  │  │  └─ features/                # Feature-specific components
│  │  │     ├─ search/
│  │  │     │  ├─ SearchResults.tsx
│  │  │     │  ├─ SearchFilters.tsx
│  │  │     │  └─ SearchSuggestions.tsx
│  │  │     │
│  │  │     ├─ recommendations/
│  │  │     │  ├─ RecommendationEngine.tsx
│  │  │     │  └─ PersonalizedOffers.tsx
│  │  │     │
│  │  │     └─ notifications/
│  │  │        ├─ NotificationCenter.tsx
│  │  │        └─ PushNotifications.tsx
│  │  │
│  │  ├─ pages/                       # Page components
│  │  │  ├─ public/                  # Public pages
│  │  │  │  ├─ HomePage.tsx
│  │  │  │  ├─ ProductsPage.tsx
│  │  │  │  ├─ ProductDetailPage.tsx
│  │  │  │  ├─ CategoryPage.tsx
│  │  │  │  ├─ SearchResultsPage.tsx
│  │  │  │  ├─ AboutPage.tsx
│  │  │  │  └─ ContactPage.tsx
│  │  │  │
│  │  │  ├─ auth/                    # Authentication pages
│  │  │  │  ├─ LoginPage.tsx
│  │  │  │  ├─ RegisterPage.tsx
│  │  │  │  └─ PasswordResetPage.tsx
│  │  │  │
│  │  │  ├─ cart/                    # Cart and checkout pages
│  │  │  │  ├─ CartPage.tsx
│  │  │  │  ├─ CheckoutPage.tsx
│  │  │  │  ├─ PaymentPage.tsx
│  │  │  │  └─ OrderConfirmationPage.tsx
│  │  │  │
│  │  │  ├─ user/                    # User account pages
│  │  │  │  ├─ UserDashboard.tsx
│  │  │  │  ├─ ProfilePage.tsx
│  │  │  │  ├─ OrderHistoryPage.tsx
│  │  │  │  ├─ WishlistPage.tsx
│  │  │  │  └─ AddressBookPage.tsx
│  │  │  │
│  │  │  ├─ admin/                   # Admin pages
│  │  │  │  ├─ AdminDashboardPage.tsx
│  │  │  │  ├─ ProductManagementPage.tsx
│  │  │  │  ├─ OrderManagementPage.tsx
│  │  │  │  ├─ UserManagementPage.tsx
│  │  │  │  └─ AnalyticsPage.tsx
│  │  │  │
│  │  │  └─ error/                   # Error pages
│  │  │     ├─ NotFoundPage.tsx
│  │  │     ├─ UnauthorizedPage.tsx
│  │  │     └─ ServerErrorPage.tsx
│  │  │
│  │  ├─ hooks/                       # Custom React hooks
│  │  │  ├─ api/                     # API-related hooks
│  │  │  │  ├─ useAuth.ts
│  │  │  │  ├─ useProducts.ts
│  │  │  │  ├─ useCart.ts
│  │  │  │  ├─ useOrders.ts
│  │  │  │  └─ useUsers.ts
│  │  │  │
│  │  │  ├─ ui/                      # UI-related hooks
│  │  │  │  ├─ useModal.ts
│  │  │  │  ├─ useToast.ts
│  │  │  │  ├─ usePagination.ts
│  │  │  │  └─ useDebounce.ts
│  │  │  │
│  │  │  ├─ business/                # Business logic hooks
│  │  │  │  ├─ useSearch.ts
│  │  │  │  ├─ useRecommendations.ts
│  │  │  │  ├─ useWishlist.ts
│  │  │  │  └─ usePayment.ts
│  │  │  │
│  │  │  └─ utils/                   # Utility hooks
│  │  │     ├─ useLocalStorage.ts
│  │  │     ├─ useWindowSize.ts
│  │  │     ├─ useIntersectionObserver.ts
│  │  │     └─ useGeolocation.ts
│  │  │
│  │  ├─ services/                    # API and external services
│  │  │  ├─ api/                     # Backend API services
│  │  │  │  ├─ client.ts             # Axios configuration
│  │  │  │  ├─ authService.ts
│  │  │  │  ├─ productService.ts
│  │  │  │  ├─ orderService.ts
│  │  │  │  ├─ userService.ts
│  │  │  │  ├─ paymentService.ts
│  │  │  │  └─ uploadService.ts
│  │  │  │
│  │  │  ├─ external/                # External service integrations
│  │  │  │  ├─ googleAnalytics.ts
│  │  │  │  ├─ stripeService.ts
│  │  │  │  ├─ socialAuthService.ts
│  │  │  │  └─ pushNotificationService.ts
│  │  │  │
│  │  │  └─ workers/                 # Service workers
│  │  │     ├─ cachingWorker.ts
│  │  │     └─ syncWorker.ts
│  │  │
│  │  ├─ store/                       # State management
│  │  │  ├─ index.ts                 # Store configuration
│  │  │  ├─ middleware/              # Custom middleware
│  │  │  │  ├─ authMiddleware.ts
│  │  │  │  └─ loggerMiddleware.ts
│  │  │  │
│  │  │  ├─ slices/                  # Redux Toolkit slices
│  │  │  │  ├─ authSlice.ts
│  │  │  │  ├─ productSlice.ts
│  │  │  │  ├─ cartSlice.ts
│  │  │  │  ├─ orderSlice.ts
│  │  │  │  ├─ userSlice.ts
│  │  │  │  ├─ uiSlice.ts
│  │  │  │  └─ searchSlice.ts
│  │  │  │
│  │  │  └─ selectors/               # Reselect selectors
│  │  │     ├─ authSelectors.ts
│  │  │     ├─ productSelectors.ts
│  │  │     ├─ cartSelectors.ts
│  │  │     └─ uiSelectors.ts
│  │  │
│  │  ├─ types/                       # TypeScript type definitions
│  │  │  ├─ api/                     # API-related types
│  │  │  │  ├─ auth.ts
│  │  │  │  ├─ product.ts
│  │  │  │  ├─ order.ts
│  │  │  │  ├─ user.ts
│  │  │  │  └─ payment.ts
│  │  │  │
│  │  │  ├─ components/              # Component prop types
│  │  │  │  ├─ common.ts
│  │  │  │  ├─ forms.ts
│  │  │  │  └─ tables.ts
│  │  │  │
│  │  │  └─ global/                  # Global type definitions
│  │  │     ├─ env.ts
│  │  │     ├─ theme.ts
│  │  │     └─ i18n.ts
│  │  │
│  │  ├─ utils/                       # Utility functions
│  │  │  ├─ constants/               # Application constants
│  │  │  │  ├─ api.ts
│  │  │  │  ├─ routes.ts
│  │  │  │  ├─ storage.ts
│  │  │  │  └─ validation.ts
│  │  │  │
│  │  │  ├─ helpers/                 # Helper functions
│  │  │  │  ├─ formatters.ts
│  │  │  │  ├─ validators.ts
│  │  │  │  ├─ calculations.ts
│  │  │  │  ├─ dateUtils.ts
│  │  │  │  └─ currencyUtils.ts
│  │  │  │
│  │  │  ├─ storage/                 # Local storage utilities
│  │  │  │  ├─ localStorage.ts
│  │  │  │  ├─ sessionStorage.ts
│  │  │  │  └─ cookieUtils.ts
│  │  │  │
│  │  │  └─ security/                # Security utilities
│  │  │     ├─ encryption.ts
│  │  │     ├─ sanitization.ts
│  │  │     └─ csrfProtection.ts
│  │  │
│  │  ├─ styles/                      # Styling and themes
│  │  │  ├─ globals.css              # Global styles
│  │  │  ├─ variables.css            # CSS variables
│  │  │  ├─ components.css           # Component-specific styles
│  │  │  ├─ animations.css           # CSS animations
│  │  │  ├─ responsive.css           # Media queries
│  │  │  │
│  │  │  ├─ themes/                  # Theme configurations
│  │  │  │  ├─ lightTheme.ts
│  │  │  │  ├─ darkTheme.ts
│  │  │  │  └─ index.ts
│  │  │  │
│  │  │  └─ mui/                     # Material-UI customization
│  │  │     ├─ muiTheme.ts
│  │  │     └─ muiOverrides.ts
│  │  │
│  │  ├─ assets/                      # Static assets
│  │  │  ├─ images/                  # Image files
│  │  │  │  ├─ logos/
│  │  │  │  ├─ icons/
│  │  │  │  ├─ banners/
│  │  │  │  └─ placeholders/
│  │  │  │
│  │  │  ├─ fonts/                   # Font files
│  │  │  │  └─ custom-fonts/
│  │  │  │
│  │  │  └─ data/                    # Static data files
│  │  │     ├─ categories.json
│  │  │     ├─ countries.json
│  │  │     └─ currencies.json
│  │  │
│  │  ├─ config/                      # Configuration files
│  │  │  ├─ environment.ts           # Environment configuration
│  │  │  ├─ api.ts                   # API configuration
│  │  │  ├─ theme.ts                 # Theme configuration
│  │  │  └─ i18n.ts                  # Internationalization setup
│  │  │
│  │  ├─ routes/                      # Routing configuration
│  │  │  ├─ AppRouter.tsx            # Main router component
│  │  │  ├─ PrivateRoute.tsx         # Protected route wrapper
│  │  │  ├─ AdminRoute.tsx           # Admin-only route wrapper
│  │  │  └─ routeConstants.ts        # Route path constants
│  │  │
│  │  ├─ contexts/                    # React contexts
│  │  │  ├─ AuthContext.tsx          # Authentication context
│  │  │  ├─ ThemeContext.tsx         # Theme context
│  │  │  ├─ CartContext.tsx          # Shopping cart context
│  │  │  └─ NotificationContext.tsx  # Notification context
│  │  │
│  │  ├─ App.tsx                     # Main App component
│  │  ├─ main.tsx                    # Application entry point
│  │  └─ vite-env.d.ts              # Vite environment types
│  │
│  ├─ tests/                         # Frontend tests
│  │  ├─ __mocks__/                  # Mock files
│  │  │  ├─ api.ts
│  │  │  └─ localStorage.ts
│  │  │
│  │  ├─ components/                 # Component tests
│  │  │  ├─ common/
│  │  │  ├─ product/
│  │  │  └─ user/
│  │  │
│  │  ├─ pages/                      # Page tests
│  │  │  ├─ HomePage.test.tsx
│  │  │  └─ ProductsPage.test.tsx
│  │  │
│  │  ├─ hooks/                      # Hook tests
│  │  │  ├─ useAuth.test.ts
│  │  │  └─ useCart.test.ts
│  │  │
│  │  ├─ utils/                      # Utility tests
│  │  │  ├─ formatters.test.ts
│  │  │  └─ validators.test.ts
│  │  │
│  │  └─ setup/                      # Test setup files
│  │     ├─ setupTests.ts
│  │     └─ testUtils.tsx
│  │
│  ├─ package.json                   # Dependencies and scripts
│  ├─ tsconfig.json                  # TypeScript configuration
│  ├─ vite.config.ts                # Vite configuration
│  ├─ tailwind.config.js            # Tailwind CSS configuration
│  ├─ eslint.config.js              # ESLint configuration
│  ├─ prettier.config.js            # Prettier configuration
│  ├─ jest.config.js                # Jest configuration
│  └─ .env.example                  # Environment variables template
│
├─ docker/                           # Docker configuration
│  ├─ docker-compose.yml             # Development environment
│  ├─ docker-compose.prod.yml        # Production environment
│  ├─ backend/
│  │  └─ Dockerfile
│  └─ frontend/
│     └─ Dockerfile
│
├─ docs/                             # Documentation
│  ├─ api/                           # API documentation
│  │  ├─ user-api.md
│  │  ├─ product-api.md
│  │  └─ order-api.md
│  │
│  ├─ database/
│  │  ├─ schema-design.md
│  │  └─ migration-guide.md
│  │
│  ├─ deployment/
│  │  ├─ docker-setup.md
│  │  └─ production-guide.md
│  │
│  └─ examples/                      # Book example codes
│     ├─ hibernate-examples/
│     │  ├─ advanced-mapping.java    # 고급 매핑 예제
│     │  └─ query-optimization.java  # 쿼리 최적화 예제
│     │
│     └─ spring-boot-examples/
│        ├─ reactive-programming.java # WebFlux 예제
│        └─ testing-strategies.java   # 테스트 전략 예제
│
├─ scripts/                          # Utility scripts
│  ├─ setup.sh                       # Environment setup
│  ├─ deploy.sh                      # Deployment script
│  └─ backup.sh                      # Database backup
│
└─ README.md                         # Project documentation
```

## 🌟 Key Features

### **E-Commerce Core**
- **Product Catalog**: Advanced product management with categories, brands, and variants
- **Shopping Cart**: Persistent cart with real-time updates and recommendations
- **Order Management**: Complete order lifecycle with status tracking
- **Payment Integration**: Multiple payment gateways (Stripe, PayPal, local methods)
- **Inventory Management**: Real-time stock tracking with automated reorder alerts

### **User Experience**
- **Multi-language Support**: i18n implementation for global reach
- **Responsive Design**: Mobile-first approach with progressive web app features
- **Search & Filter**: Elasticsearch-powered advanced product search
- **Wishlist & Reviews**: Customer engagement features with rating system
- **Recommendation Engine**: ML-powered product recommendations

### **Admin Features**
- **Dashboard Analytics**: Sales, inventory, and customer insights
- **Content Management**: Product, category, and brand management
- **Order Processing**: Order fulfillment and shipping management
- **Customer Support**: Integrated ticketing and chat system
- **Reporting**: Comprehensive business intelligence reports

## ⏳ Project Timeline & Milestones
- **Start Date**: 2025-08-15
- **MVP Completion**: 2025-09-05
- **Production Deploy**: 2025-09-10

### Updates Log
```
2025-08-15 - Project initialization and backend architecture setup
2025-08-17 - Hibernate entities and database schema implementation
2025-08-19 - Core REST APIs and authentication system
2025-08-22 - Payment gateway integration and order processing
2025-08-25 - React frontend foundation and component library
2025-08-28 - Frontend-backend integration and state management
2025-09-02 - Testing, optimization, and security hardening
2025-09-05 - Documentation completion and deployment preparation
```

## 🚀 Getting Started

### Prerequisites
- JDK 21 or higher
- Node.js 18+ and npm/yarn
- PostgreSQL 15+
- Redis 7+
- Docker & Docker Compose (recommended)

### Quick Start with Docker
```bash
# Clone the repository
git clone https://github.com/yourusername/sb3-react-animalduo.git
cd sb3-react-animalduo

# Start the development environment
docker-compose up -d

# The application will be available at:
# Frontend: http://localhost:3000
# Backend API: http://localhost:8080
# API Documentation: http://localhost:8080/swagger-ui.html
```

### Manual Setup

#### Backend Setup
```bash
cd backend

# Configure database
cp src/main/resources/application-dev.yml.example src/main/resources/application-dev.yml
# Edit database credentials

# Run the application
./mvnw spring-boot:run -Dspring-boot.run.profiles=dev
```

#### Frontend Setup
```bash
cd frontend

# Install dependencies
npm install

# Start development server
npm run dev
```

## 🗄 Database Schema

### Core Entities (Hibernate Examples)

#### User Entity with Advanced Mapping
```java
@Entity
@Table(name = "users")
@Cache(usage = CacheConcurrencyStrategy.READ_WRITE)
public class User extends BaseEntity {
    
    @Id
    @GeneratedValue(strategy = GenerationType.IDENTITY)
    private Long id;
    
    @Column(unique = true, nullable = false)
    private String email;
    
    @OneToMany(mappedBy = "user", cascade = CascadeType.ALL, fetch = FetchType.LAZY)
    @Cache(usage = CacheConcurrencyStrategy.READ_WRITE)
    private Set<UserAddress> addresses = new LinkedHashSet<>();
    
    @OneToMany(mappedBy = "customer", cascade = CascadeType.ALL)
    private List<Order> orders = new ArrayList<>();
    
    @ManyToMany(fetch = FetchType.EAGER)
    @JoinTable(
        name = "user_roles",
        joinColumns = @JoinColumn(name = "user_id"),
        inverseJoinColumns = @JoinColumn(name = "role_id")
    )
    private Set<Role> roles = new HashSet<>();
}
```

#### Product Entity with Inheritance
```java
@Entity
@Table(name = "products")
@Inheritance(strategy = InheritanceType.JOINED)
@DiscriminatorColumn(name = "product_type")
public abstract class Product extends BaseEntity {
    
    @Id
    @GeneratedValue(strategy = GenerationType.IDENTITY)
    private Long id;
    
    @Column(nullable = false)
    private String name;
    
    @Column(columnDefinition = "TEXT")
    private String description;
    
    @Column(precision = 10, scale = 2)
    private BigDecimal price;
    
    @ManyToOne(fetch = FetchType.LAZY)
    @JoinColumn(name = "category_id")
    private Category category;
    
    @OneToMany(mappedBy = "product", cascade = CascadeType.ALL, orphanRemoval = true)
    private List<ProductImage> images = new ArrayList<>();
    
    @ElementCollection
    @CollectionTable(name = "product_tags")
    private Set<String> tags = new HashSet<>();
}
```

## 🧪 Testing Strategy

### Test Configuration
```yaml
# application-test.yml
spring:
  datasource:
    url: jdbc:h2:mem:testdb
    driver-class-name: org.h2.Driver
  jpa:
    hibernate:
      ddl-auto: create-drop
  test:
    database:
      replace: none
```

### Integration Test Example
```java
@SpringBootTest(webEnvironment = SpringBootTest.WebEnvironment.RANDOM_PORT)
@Testcontainers
@ActiveProfiles("test")
class ProductControllerIntegrationTest {
    
    @Container
    static PostgreSQLContainer<?> postgres = new PostgreSQLContainer<>("postgres:15")
            .withDatabaseName("testdb")
            .withUsername("test")
            .withPassword("test");
    
    @Autowired
    private TestRestTemplate restTemplate;
    
    @Test
    void shouldCreateProduct() {
        // Test implementation
    }
}
```

## 📚 References

#### 📖 Books & Documentation
- [Spring Boot 3 in Action](https://www.manning.com/books/spring-boot-in-action)
- [Hibernate ORM 6 Documentation](https://hibernate.org/orm/documentation/6.4/)
- [React 18 Documentation](https://react.dev/)
- [TypeScript Handbook](https://www.typescriptlang.org/docs/)

#### 🛠 Framework Documentation
- [Spring Boot 3 Reference](https://docs.spring.io/spring-boot/docs/current/reference/html/)
- [Spring Security 6](https://docs.spring.io/spring-security/reference/)
- [Spring Data JPA](https://docs.spring.io/spring-data/jpa/docs/current/reference/html/)
- [Material-UI (MUI)](https://mui.com/material-ui/getting-started/overview/)

#### 🌐 Community & Tools
- [Spring Boot Guides](https://spring.io/guides)
- [Hibernate Community](https://hibernate.org/community/)
- [React Community](https://react.dev/community)
- [Stack Overflow - Spring Boot](https://stackoverflow.com/questions/tagged/spring-boot)

## 🏗 Architecture Patterns

### Layered Architecture
```
Presentation Layer (Controllers) 
    ↓
Business Layer (Services)
    ↓
Persistence Layer (Repositories)
    ↓
Database Layer (PostgreSQL)
```

### Security Architecture
- JWT-based authentication
- Role-based authorization (RBAC)
- CORS configuration for React frontend
- Rate limiting and DDoS protection
- Input validation and sanitization

## 📊 Performance Optimization

### Backend Optimizations
- **Hibernate**: Second-level caching with Ehcache
- **Database**: Connection pooling with HikariCP
- **Caching**: Redis for session and application data
- **API**: Pagination and lazy loading strategies

### Frontend Optimizations
- **Code Splitting**: Route-based lazy loading
- **State Management**: Optimized Redux selectors
- **Caching**: React Query for server state
- **Bundle**: Webpack optimization and tree shaking

## 🤝 Contributing
Please read [CONTRIBUTING.md](docs/contributing.md) for details on our code of conduct and the process for submitting pull requests.

## 📄 License
This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
