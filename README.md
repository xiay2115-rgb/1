<!DOCTYPE html>
<html lang="zh-CN">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>跨境独立站 - Shopline主题</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0/css/all.min.css">
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }
        
        :root {
            --primary: #2c3e50;
            --secondary: #3498db;
            --accent: #e74c3c;
            --light: #ecf0f1;
            --dark: #2c3e50;
            --gray: #95a5a6;
            --text: #333333;
            --white: #ffffff;
            --shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
            --transition: all 0.3s ease;
        }
        
        body {
            color: var(--text);
            line-height: 1.6;
            background-color: var(--light);
        }
        
        .container {
            width: 100%;
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 20px;
        }
        
        /* 导航栏样式 */
        header {
            background-color: var(--white);
            box-shadow: var(--shadow);
            position: sticky;
            top: 0;
            z-index: 1000;
        }
        
        .navbar {
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 20px 0;
        }
        
        .logo {
            font-size: 24px;
            font-weight: 700;
            color: var(--primary);
            text-decoration: none;
        }
        
        .nav-links {
            display: flex;
            list-style: none;
        }
        
        .nav-links li {
            margin-left: 30px;
        }
        
        .nav-links a {
            text-decoration: none;
            color: var(--dark);
            font-weight: 500;
            transition: var(--transition);
        }
        
        .nav-links a:hover {
            color: var(--secondary);
        }
        
        .nav-icons {
            display: flex;
            align-items: center;
        }
        
        .nav-icons i {
            margin-left: 20px;
            font-size: 20px;
            color: var(--dark);
            cursor: pointer;
            transition: var(--transition);
        }
        
        .nav-icons i:hover {
            color: var(--secondary);
        }
        
        .mobile-menu {
            display: none;
            font-size: 24px;
            cursor: pointer;
        }
        
        /* 英雄区域样式 */
        .hero {
            background: linear-gradient(rgba(44, 62, 80, 0.8), rgba(44, 62, 80, 0.8)), url('https://images.unsplash.com/photo-1607082348824-0a96f2a4b9da?ixlib=rb-1.2.1&auto=format&fit=crop&w=1350&q=80');
            background-size: cover;
            background-position: center;
            color: var(--white);
            padding: 100px 0;
            text-align: center;
        }
        
        .hero h1 {
            font-size: 48px;
            margin-bottom: 20px;
        }
        
        .hero p {
            font-size: 20px;
            max-width: 700px;
            margin: 0 auto 30px;
        }
        
        .btn {
            display: inline-block;
            background-color: var(--accent);
            color: var(--white);
            padding: 12px 30px;
            border-radius: 30px;
            text-decoration: none;
            font-weight: 600;
            transition: var(--transition);
            border: none;
            cursor: pointer;
        }
        
        .btn:hover {
            background-color: #c0392b;
            transform: translateY(-3px);
        }
        
        /* 特色区域样式 */
        .features {
            padding: 80px 0;
            background-color: var(--white);
        }
        
        .section-title {
            text-align: center;
            margin-bottom: 50px;
        }
        
        .section-title h2 {
            font-size: 36px;
            color: var(--primary);
            margin-bottom: 15px;
        }
        
        .section-title p {
            color: var(--gray);
            max-width: 600px;
            margin: 0 auto;
        }
        
        .features-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 30px;
        }
        
        .feature-card {
            background-color: var(--white);
            border-radius: 10px;
            padding: 30px;
            text-align: center;
            box-shadow: var(--shadow);
            transition: var(--transition);
        }
        
        .feature-card:hover {
            transform: translateY(-10px);
        }
        
        .feature-icon {
            font-size: 40px;
            color: var(--secondary);
            margin-bottom: 20px;
        }
        
        .feature-card h3 {
            font-size: 22px;
            margin-bottom: 15px;
            color: var(--primary);
        }
        
        /* 产品展示样式 */
        .products {
            padding: 80px 0;
            background-color: var(--light);
        }
        
        .products-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 30px;
        }
        
        .product-card {
            background-color: var(--white);
            border-radius: 10px;
            overflow: hidden;
            box-shadow: var(--shadow);
            transition: var(--transition);
        }
        
        .product-card:hover {
            transform: translateY(-5px);
        }
        
        .product-img {
            height: 200px;
            background-color: #f5f5f5;
            display: flex;
            align-items: center;
            justify-content: center;
            overflow: hidden;
        }
        
        .product-img img {
            width: 100%;
            height: 100%;
            object-fit: cover;
            transition: var(--transition);
        }
        
        .product-card:hover .product-img img {
            transform: scale(1.1);
        }
        
        .product-info {
            padding: 20px;
        }
        
        .product-info h3 {
            font-size: 18px;
            margin-bottom: 10px;
        }
        
        .product-price {
            color: var(--accent);
            font-weight: 700;
            font-size: 20px;
            margin-bottom: 15px;
        }
        
        /* 品牌故事样式 */
        .brand-story {
            padding: 80px 0;
            background-color: var(--white);
        }
        
        .story-content {
            display: flex;
            align-items: center;
            gap: 50px;
        }
        
        .story-text {
            flex: 1;
        }
        
        .story-text h2 {
            font-size: 36px;
            color: var(--primary);
            margin-bottom: 20px;
        }
        
        .story-text p {
            margin-bottom: 20px;
        }
        
        .story-image {
            flex: 1;
            border-radius: 10px;
            overflow: hidden;
            box-shadow: var(--shadow);
        }
        
        .story-image img {
            width: 100%;
            height: auto;
            display: block;
        }
        
        /* 新闻通讯样式 */
        .newsletter {
            padding: 80px 0;
            background-color: var(--primary);
            color: var(--white);
            text-align: center;
        }
        
        .newsletter h2 {
            font-size: 36px;
            margin-bottom: 20px;
        }
        
        .newsletter p {
            max-width: 600px;
            margin: 0 auto 30px;
        }
        
        .newsletter-form {
            display: flex;
            max-width: 500px;
            margin: 0 auto;
        }
        
        .newsletter-form input {
            flex: 1;
            padding: 15px;
            border: none;
            border-radius: 30px 0 0 30px;
            font-size: 16px;
        }
        
        .newsletter-form button {
            background-color: var(--accent);
            color: var(--white);
            border: none;
            padding: 0 30px;
            border-radius: 0 30px 30px 0;
            cursor: pointer;
            font-weight: 600;
            transition: var(--transition);
        }
        
        .newsletter-form button:hover {
            background-color: #c0392b;
        }
        
        /* 页脚样式 */
        footer {
            background-color: var(--dark);
            color: var(--white);
            padding: 60px 0 20px;
        }
        
        .footer-content {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
            gap: 40px;
            margin-bottom: 40px;
        }
        
        .footer-column h3 {
            font-size: 20px;
            margin-bottom: 20px;
            position: relative;
            padding-bottom: 10px;
        }
        
        .footer-column h3::after {
            content: '';
            position: absolute;
            left: 0;
            bottom: 0;
            width: 40px;
            height: 2px;
            background-color: var(--secondary);
        }
        
        .footer-column ul {
            list-style: none;
        }
        
        .footer-column ul li {
            margin-bottom: 10px;
        }
        
        .footer-column a {
            color: var(--gray);
            text-decoration: none;
            transition: var(--transition);
        }
        
        .footer-column a:hover {
            color: var(--secondary);
        }
        
        .social-icons {
            display: flex;
            gap: 15px;
            margin-top: 20px;
        }
        
        .social-icons a {
            display: flex;
            align-items: center;
            justify-content: center;
            width: 40px;
            height: 40px;
            background-color: rgba(255, 255, 255, 0.1);
            border-radius: 50%;
            transition: var(--transition);
        }
        
        .social-icons a:hover {
            background-color: var(--secondary);
            transform: translateY(-5px);
        }
        
        .copyright {
            text-align: center;
            padding-top: 20px;
            border-top: 1px solid rgba(255, 255, 255, 0.1);
            color: var(--gray);
            font-size: 14px;
        }
        
        /* 响应式设计 */
        @media (max-width: 992px) {
            .story-content {
                flex-direction: column;
            }
            
            .story-image {
                order: -1;
            }
        }
        
        @media (max-width: 768px) {
            .nav-links {
                display: none;
            }
            
            .mobile-menu {
                display: block;
            }
            
            .hero h1 {
                font-size: 36px;
            }
            
            .hero p {
                font-size: 18px;
            }
            
            .newsletter-form {
                flex-direction: column;
            }
            
            .newsletter-form input {
                border-radius: 30px;
                margin-bottom: 10px;
            }
            
            .newsletter-form button {
                border-radius: 30px;
                padding: 15px;
            }
        }
    </style>
</head>
<body>
    <!-- 导航栏 -->
    <header>
        <div class="container">
            <nav class="navbar">
                <a href="#" class="logo">GlobalShop</a>
                
                <ul class="nav-links">
                    <li><a href="#">首页</a></li>
                    <li><a href="#">产品</a></li>
                    <li><a href="#">分类</a></li>
                    <li><a href="#">品牌故事</a></li>
                    <li><a href="#">联系我们</a></li>
                </ul>
                
                <div class="nav-icons">
                    <i class="fas fa-search"></i>
                    <i class="fas fa-user"></i>
                    <i class="fas fa-shopping-cart"></i>
                    <div class="mobile-menu">
                        <i class="fas fa-bars"></i>
                    </div>
                </div>
            </nav>
        </div>
    </header>

    <!-- 英雄区域 -->
    <section class="hero">
        <div class="container">
            <h1>全球精选优质商品</h1>
            <p>我们致力于为您提供来自世界各地的优质商品，让您足不出户即可享受全球购物体验</p>
            <a href="#" class="btn">立即购买</a>
        </div>
    </section>

    <!-- 特色区域 -->
    <section class="features">
        <div class="container">
            <div class="section-title">
                <h2>为什么选择我们</h2>
                <p>我们为您提供最优质的购物体验和最贴心的客户服务</p>
            </div>
            
            <div class="features-grid">
                <div class="feature-card">
                    <div class="feature-icon">
                        <i class="fas fa-globe"></i>
                    </div>
                    <h3>全球直采</h3>
                    <p>我们与全球优质供应商合作，确保每一件商品都是正品，质量有保障。</p>
                </div>
                
                <div class="feature-card">
                    <div class="feature-icon">
                        <i class="fas fa-shipping-fast"></i>
                    </div>
                    <h3>快速配送</h3>
                    <p>与全球顶级物流公司合作，确保您的订单快速安全地送达。</p>
                </div>
                
                <div class="feature-card">
                    <div class="feature-icon">
                        <i class="fas fa-headset"></i>
                    </div>
                    <h3>24/7 客服</h3>
                    <p>我们的客服团队全天候为您服务，解答您的任何疑问。</p>
                </div>
            </div>
        </div>
    </section>

    <!-- 产品展示 -->
    <section class="products">
        <div class="container">
            <div class="section-title">
                <h2>热门产品</h2>
                <p>探索我们最受欢迎的产品系列</p>
            </div>
            
            <div class="products-grid">
                <div class="product-card">
                    <div class="product-img">
                        <img src="https://images.unsplash.com/photo-1523275335684-37898b6baf30?ixlib=rb-1.2.1&auto=format&fit=crop&w=500&q=60" alt="智能手表">
                    </div>
                    <div class="product-info">
                        <h3>智能手表 Pro</h3>
                        <div class="product-price">¥899</div>
                        <a href="#" class="btn">加入购物车</a>
                    </div>
                </div>
                
                <div class="product-card">
                    <div class="product-img">
                        <img src="https://images.unsplash.com/photo-1505740420928-5e560c06d30e?ixlib=rb-1.2.1&auto=format&fit=crop&w=500&q=60" alt="无线耳机">
                    </div>
                    <div class="product-info">
                        <h3>无线降噪耳机</h3>
                        <div class="product-price">¥699</div>
                        <a href="#" class="btn">加入购物车</a>
                    </div>
                </div>
                
                <div class="product-card">
                    <div class="product-img">
                        <img src="https://images.unsplash.com/photo-1546868871-7041f2a55e12?ixlib=rb-1.2.1&auto=format&fit=crop&w=500&q=60" alt="便携音箱">
                    </div>
                    <div class="product-info">
                        <h3>便携蓝牙音箱</h3>
                        <div class="product-price">¥399</div>
                        <a href="#" class="btn">加入购物车</a>
                    </div>
                </div>
                
                <div class="product-card">
                    <div class="product-img">
                        <img src="https://images.unsplash.com/photo-1542291026-7eec264c27ff?ixlib=rb-1.2.1&auto=format&fit=crop&w=500&q=60" alt="运动鞋">
                    </div>
                    <div class="product-info">
                        <h3>专业运动跑鞋</h3>
                        <div class="product-price">¥599</div>
                        <a href="#" class="btn">加入购物车</a>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- 品牌故事 -->
    <section class="brand-story">
        <div class="container">
            <div class="story-content">
                <div class="story-text">
                    <h2>我们的品牌故事</h2>
                    <p>GlobalShop成立于2018年，我们的使命是打破地理界限，让全球优质商品触手可及。我们相信，无论您身在何处，都应该能够享受到世界各地的优质产品。</p>
                    <p>我们的团队遍布全球，精心挑选每一件商品，确保它们符合我们的高质量标准。从电子产品到时尚单品，从家居用品到健康食品，我们致力于为您提供最优质的选择。</p>
                    <p>我们不仅是一个电商平台，更是连接全球消费者与优质商品的桥梁。感谢您选择GlobalShop，我们期待为您提供卓越的购物体验。</p>
                    <a href="#" class="btn">了解更多</a>
                </div>
                <div class="story-image">
                    <img src="https://images.unsplash.com/photo-1556742049-0cfed4f6a45d?ixlib=rb-1.2.1&auto=format&fit=crop&w=500&q=60" alt="品牌故事">
                </div>
            </div>
        </div>
    </section>

    <!-- 新闻通讯 -->
    <section class="newsletter">
        <div class="container">
            <h2>订阅我们的通讯</h2>
            <p>获取最新产品信息、独家优惠和购物指南</p>
            <form class="newsletter-form">
                <input type="email" placeholder="请输入您的邮箱地址" required>
                <button type="submit">订阅</button>
            </form>
        </div>
    </section>

    <!-- 页脚 -->
    <footer>
        <div class="container">
            <div class="footer-content">
                <div class="footer-column">
                    <h3>关于我们</h3>
                    <ul>
                        <li><a href="#">品牌故事</a></li>
                        <li><a href="#">团队介绍</a></li>
                        <li><a href="#">职业机会</a></li>
                        <li><a href="#">新闻中心</a></li>
                    </ul>
                </div>
                
                <div class="footer-column">
                    <h3>客户服务</h3>
                    <ul>
                        <li><a href="#">帮助中心</a></li>
                        <li><a href="#">配送信息</a></li>
                        <li><a href="#">退换政策</a></li>
                        <li><a href="#">联系我们</a></li>
                    </ul>
                </div>
                
                <div class="footer-column">
                    <h3>购物指南</h3>
                    <ul>
                        <li><a href="#">如何购买</a></li>
                        <li><a href="#">支付方式</a></li>
                        <li><a href="#">会员制度</a></li>
                        <li><a href="#">常见问题</a></li>
                    </ul>
                </div>
                
                <div class="footer-column">
                    <h3>联系信息</h3>
                    <ul>
                        <li><i class="fas fa-map-marker-alt"></i> 上海市浦东新区张江高科技园区</li>
                        <li><i class="fas fa-phone"></i> 400-123-4567</li>
                        <li><i class="fas fa-envelope"></i> info@globalshop.com</li>
                    </ul>
                    <div class="social-icons">
                        <a href="#"><i class="fab fa-weixin"></i></a>
                        <a href="#"><i class="fab fa-weibo"></i></a>
                        <a href="#"><i class="fab fa-instagram"></i></a>
                        <a href="#"><i class="fab fa-tiktok"></i></a>
                    </div>
                </div>
            </div>
            
            <div class="copyright">
                <p>&copy; 2023 GlobalShop 跨境独立站. 保留所有权利.</p>
            </div>
        </div>
    </footer>

    <script>
        // 移动端菜单切换
        document.querySelector('.mobile-menu').addEventListener('click', function() {
            document.querySelector('.nav-links').classList.toggle('active');
        });
        
        // 简单的图片懒加载
        document.addEventListener('DOMContentLoaded', function() {
            const images = document.querySelectorAll('img');
            
            const imageObserver = new IntersectionObserver((entries, observer) => {
                entries.forEach(entry => {
                    if (entry.isIntersecting) {
                        const img = entry.target;
                        img.src = img.dataset.src;
                        imageObserver.unobserve(img);
                    }
                });
            });
            
            images.forEach(img => {
                if (img.dataset.src) {
                    imageObserver.observe(img);
                }
            });
        });
    </script>
</body>
</html>
