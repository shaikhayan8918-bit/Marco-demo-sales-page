# Marco-demo-sales-page
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Scale Your SMMA to $30k/Month</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Inter', -apple-system, BlinkMacSystemFont, sans-serif;
            line-height: 1.6;
            color: #ffffff;
            background: linear-gradient(135deg, #0a0a0a 0%, #1a1a2e 50%, #16213e 100%);
            overflow-x: hidden;
        }

        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 20px;
        }

        .hero {
            min-height: 100vh;
            display: flex;
            align-items: center;
            position: relative;
            background: radial-gradient(circle at 50% 0%, rgba(120, 119, 198, 0.1) 0%, transparent 50%);
        }

        .hero::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            bottom: 0;
            background: url('data:image/svg+xml,<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 100 100"><defs><pattern id="grain" width="100" height="100" patternUnits="userSpaceOnUse"><circle cx="25" cy="25" r="0.5" fill="%23ffffff" opacity="0.05"/><circle cx="75" cy="25" r="0.5" fill="%23ffffff" opacity="0.05"/><circle cx="50" cy="50" r="0.5" fill="%23ffffff" opacity="0.05"/><circle cx="25" cy="75" r="0.5" fill="%23ffffff" opacity="0.05"/><circle cx="75" cy="75" r="0.5" fill="%23ffffff" opacity="0.05"/></pattern></defs><rect width="100" height="100" fill="url(%23grain)"/></svg>');
            pointer-events: none;
        }

        .preheader {
            display: inline-block;
            background: linear-gradient(90deg, #ff6b6b, #ffd93d);
            color: #000;
            padding: 8px 24px;
            border-radius: 30px;
            font-weight: 700;
            font-size: 14px;
            text-transform: uppercase;
            letter-spacing: 0.5px;
            margin-bottom: 24px;
            animation: pulse 2s infinite;
        }

        @keyframes pulse {
            0%, 100% { transform: scale(1); }
            50% { transform: scale(1.05); }
        }

        .hero-content {
            position: relative;
            z-index: 2;
        }

        .hero h1 {
            font-size: clamp(2.5rem, 5vw, 4.5rem);
            font-weight: 900;
            line-height: 1.1;
            margin-bottom: 24px;
            background: linear-gradient(135deg, #ffffff 0%, #a8a8a8 100%);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
        }

        .hero .subheader {
            font-size: clamp(1.2rem, 2.5vw, 1.8rem);
            color: #b0b0b0;
            margin-bottom: 40px;
            line-height: 1.4;
        }

        .vsl-placeholder {
            background: linear-gradient(135deg, #1a1a2e 0%, #16213e 100%);
            border: 2px solid rgba(255, 255, 255, 0.1);
            border-radius: 20px;
            padding: 80px 40px;
            text-align: center;
            margin: 40px 0;
            backdrop-filter: blur(10px);
        }

        .cta-primary {
            display: inline-block;
            background: linear-gradient(135deg, #ff6b6b 0%, #ffd93d 100%);
            color: #000;
            padding: 20px 50px;
            border: none;
            border-radius: 50px;
            font-size: 1.2rem;
            font-weight: 800;
            text-decoration: none;
            text-transform: uppercase;
            letter-spacing: 1px;
            transition: all 0.3s ease;
            box-shadow: 0 10px 30px rgba(255, 107, 107, 0.3);
            margin-top: 20px;
        }

        .cta-primary:hover {
            transform: translateY(-3px);
            box-shadow: 0 20px 40px rgba(255, 107, 107, 0.4);
        }

        .section {
            padding: 100px 0;
            position: relative;
        }

        .section:nth-child(even) {
            background: linear-gradient(135deg, rgba(26, 26, 46, 0.5) 0%, rgba(22, 33, 62, 0.5) 100%);
        }

        .section-header {
            font-size: clamp(2rem, 4vw, 3.5rem);
            font-weight: 800;
            margin-bottom: 60px;
            text-align: center;
            background: linear-gradient(135deg, #ff6b6b 0%, #ffd93d 100%);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
        }

        .content-block {
            max-width: 800px;
            margin: 0 auto;
            font-size: 1.1rem;
            line-height: 1.8;
        }

        .content-block p {
            margin-bottom: 20px;
        }

        .content-block strong {
            color: #ff6b6b;
            font-weight: 700;
        }

        .highlight {
            background: linear-gradient(90deg, rgba(255, 107, 107, 0.2), rgba(255, 217, 61, 0.2));
            padding: 30px;
            border-radius: 15px;
            border-left: 4px solid #ff6b6b;
            margin: 40px 0;
            backdrop-filter: blur(10px);
        }

        .feature-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(350px, 1fr));
            gap: 30px;
            margin: 60px 0;
        }

        .feature-card {
            background: linear-gradient(135deg, rgba(255, 255, 255, 0.05) 0%, rgba(255, 255, 255, 0.02) 100%);
            border: 1px solid rgba(255, 255, 255, 0.1);
            border-radius: 20px;
            padding: 40px;
            backdrop-filter: blur(20px);
            transition: all 0.3s ease;
        }

        .feature-card:hover {
            transform: translateY(-10px);
            border-color: rgba(255, 107, 107, 0.3);
            box-shadow: 0 20px 40px rgba(0, 0, 0, 0.2);
        }

        .feature-card h3 {
            color: #ff6b6b;
            font-size: 1.3rem;
            font-weight: 700;
            margin-bottom: 15px;
        }

        .faq-item {
            background: linear-gradient(135deg, rgba(255, 255, 255, 0.05) 0%, rgba(255, 255, 255, 0.02) 100%);
            border-radius: 15px;
            padding: 30px;
            margin-bottom: 20px;
            border-left: 4px solid #ffd93d;
        }

        .faq-question {
            font-weight: 700;
            font-size: 1.2rem;
            color: #ffd93d;
            margin-bottom: 15px;
        }

        .guarantee-box {
            background: linear-gradient(135deg, #16213e 0%, #1a1a2e 100%);
            border: 2px solid #ff6b6b;
            border-radius: 20px;
            padding: 50px;
            text-align: center;
            margin: 60px 0;
            position: relative;
            overflow: hidden;
        }

        .guarantee-box::before {
            content: '';
            position: absolute;
            top: -2px;
            left: -2px;
            right: -2px;
            bottom: -2px;
            background: linear-gradient(45deg, #ff6b6b, #ffd93d, #ff6b6b);
            border-radius: 20px;
            z-index: -1;
            animation: border-glow 3s linear infinite;
        }

        @keyframes border-glow {
            0% { background-position: 0% 50%; }
            100% { background-position: 100% 50%; }
        }

        .cta-section {
            text-align: center;
            padding: 100px 0;
            background: linear-gradient(135deg, rgba(255, 107, 107, 0.1) 0%, rgba(255, 217, 61, 0.1) 100%);
        }

        .floating-elements {
            position: absolute;
            width: 100%;
            height: 100%;
            overflow: hidden;
            pointer-events: none;
        }

        .floating-element {
            position: absolute;
            border-radius: 50%;
            background: linear-gradient(135deg, rgba(255, 107, 107, 0.1), rgba(255, 217, 61, 0.1));
            animation: float 6s ease-in-out infinite;
        }

        .floating-element:nth-child(1) {
            width: 80px;
            height: 80px;
            top: 20%;
            left: 10%;
            animation-delay: -2s;
        }

        .floating-element:nth-child(2) {
            width: 60px;
            height: 60px;
            top: 60%;
            right: 10%;
            animation-delay: -1s;
        }

        .floating-element:nth-child(3) {
            width: 100px;
            height: 100px;
            top: 80%;
            left: 20%;
            animation-delay: -3s;
        }

        @keyframes float {
            0%, 100% { transform: translateY(0px) rotate(0deg); }
            50% { transform: translateY(-20px) rotate(180deg); }
        }

        @media (max-width: 768px) {
            .hero {
                padding: 100px 0 50px;
                min-height: auto;
            }
            
            .section {
                padding: 60px 0;
            }
            
            .feature-grid {
                grid-template-columns: 1fr;
            }
        }
    </style>
</head>
<body>
    <div class="floating-elements">
        <div class="floating-element"></div>
        <div class="floating-element"></div>
        <div class="floating-element"></div>
    </div>

    <section class="hero">
        <div class="container">
            <div class="hero-content">
                <div class="preheader">ATTENTION: Struggling SMMA Owners & Aspiring Agency Entrepreneurs</div>
                <h1>Scale Your Social Media Marketing Agency From $0 to $30k/Month in Record Time</h1>
                <p class="subheader">Without wasting months on trial-and-error, getting stuck in endless client acquisition struggles, or burning out from trying to do everything yourself</p>
                
                <div class="vsl-placeholder">
                    <h3 style="color: #ff6b6b; margin-bottom: 20px;">🎥 Watch This Exclusive Training Video</h3>
                    <p style="color: #b0b0b0;">Discover the exact step-by-step system that's helping SMMA owners finally break through their revenue ceiling</p>
                </div>
                
                <a href="#" class="cta-primary">Book Your Strategy Call Now</a>
            </div>
        </div>
    </section>

    <section class="section">
        <div class="container">
            <h2 class="section-header">Here's the brutal truth about why 97% of SMMA owners never break $10k/month...</h2>
            <div class="content-block">
                <p>You're drowning in the day-to-day chaos.</p>
                <p>Scrambling to find clients who actually pay on time.</p>
                <p>Staying up until 2 AM wondering if that prospect will ever text you back...</p>
                <p><strong>And deep down, you know you're just one difficult client away from having to explain to your family why the "big opportunity" didn't work out.</strong></p>
                
                <div class="highlight">
                    <p><strong>Sound familiar?</strong></p>
                    <p>Here's what nobody tells you about running an SMMA: <strong>It's not about working harder. It's about having a SYSTEM.</strong></p>
                </div>
                
                <p>Most agency owners are stuck playing whack-a-mole with their business...</p>
                <p>Frantically sending cold DMs that get ignored.</p>
                <p>Jumping on discovery calls with broke prospects who "need to think about it."</p>
                <p>Delivering mediocre results because you're spread too thin across everything.</p>
                
                <p><strong>But what if there was a different way?</strong></p>
                <p>What if you could book 45+ qualified appointments every month... systematically close high-paying clients... and scale to $30k/month without the constant stress and overwhelm?</p>
            </div>
        </div>
    </section>

    <section class="section">
        <div class="container">
            <h2 class="section-header">The day everything changed for me (and why I almost quit my agency)</h2>
            <div class="content-block">
                <p>Three years ago, I was exactly where you are right now.</p>
                <p><strong>Broke. Frustrated. Ready to throw in the towel.</strong></p>
                
                <p>I'd spent months trying to "crack the code" on client acquisition...</p>
                <p>Watching YouTube videos until my eyes bled.</p>
                <p>Buying course after course from "gurus" who hadn't run an active agency in years.</p>
                <p>Following outdated strategies that worked in 2019 but left me with a 2% response rate in today's market.</p>
                
                <div class="highlight">
                    <p>I was hemorrhaging money, losing confidence, and my girlfriend was starting to ask some very uncomfortable questions about when I'd "get a real job."</p>
                </div>
                
                <p>That's when I discovered something that changed everything...</p>
                <p><strong>The problem wasn't my work ethic. It wasn't my skills. It wasn't even my offers.</strong></p>
                <p><strong>The problem was I was trying to build a Ferrari with bicycle parts.</strong></p>
                
                <p>See, most SMMA owners approach client acquisition like they're playing the lottery...</p>
                <p>Send 100 random DMs and pray someone responds.</p>
                <p>But successful agencies? They operate like <strong>precision machines.</strong></p>
                
                <p>Every outreach message has been tested and optimized.</p>
                <p>Every sales conversation follows a proven framework.</p>
                <p>Every service delivery process is systematized for maximum results.</p>
                
                <div class="highlight">
                    <p><strong>Once I cracked this code and built my own "precision machine," everything shifted...</strong></p>
                    <p>From 2 clients struggling to pay me $500/month...</p>
                    <p>To 45+ qualified appointments every single month.</p>
                    <p>From begging prospects to work with me...</p>
                    <p>To having a waitlist of businesses ready to pay premium prices.</p>
                    <p>From working 16-hour days just to stay afloat...</p>
                    <p>To running a $30k/month agency that practically runs itself.</p>
                </div>
            </div>
        </div>
    </section>

    <section class="section">
        <div class="container">
            <h2 class="section-header">The complete roadmap that transforms struggling agency owners into client-attracting machines</h2>
            <div class="content-block">
                <p>This isn't another "mindset course" or collection of outdated tactics.</p>
                <p><strong>This is the exact step-by-step system I use to run my own profitable SMMA...</strong></p>
                <p><strong>And the same system I've used to help dozens of agency owners finally break through their revenue ceiling.</strong></p>
                
                <div class="feature-grid">
                    <div class="feature-card">
                        <h3>✓ Active Agency Owner</h3>
                        <p>I'm not some retired "guru" selling you recycled strategies from 2018. I'm actively running my own agency RIGHT NOW using these exact methods.</p>
                    </div>
                    
                    <div class="feature-card">
                        <h3>✓ Automated Systems</h3>
                        <p>This isn't about sending more cold DMs or "hustling harder." It's about building automated systems that attract qualified prospects like a magnet.</p>
                    </div>
                    
                    <div class="feature-card">
                        <h3>✓ Complete Transformation</h3>
                        <p>I don't just teach client acquisition. I show you how to deliver jaw-dropping results that turn one-time clients into long-term partnerships.</p>
                    </div>
                </div>
                
                <div class="highlight">
                    <p><strong>The result?</strong></p>
                    <p>A complete transformation from overwhelmed solopreneur to confident agency owner with a predictable, scalable business.</p>
                </div>
            </div>
        </div>
    </section>

    <section class="section">
        <div class="container">
            <h2 class="section-header">Here's exactly what you get when you book your strategy call:</h2>
            <div class="feature-grid">
                <div class="feature-card">
                    <h3>✓ The High-Volume Prospecting Framework</h3>
                    <p>How to generate 45+ qualified appointments per month without spending hours manually sending DMs</p>
                </div>
                
                <div class="feature-card">
                    <h3>✓ The Trust-Building Outreach System</h3>
                    <p>The exact message templates and follow-up sequences that turn cold prospects into warm leads</p>
                </div>
                
                <div class="feature-card">
                    <h3>✓ The Premium Offer Creation Blueprint</h3>
                    <p>How to package your services so prospects see you as the obvious choice (even at higher prices)</p>
                </div>
                
                <div class="feature-card">
                    <h3>✓ The Bulletproof Sales Process</h3>
                    <p>Step-by-step scripts and frameworks for closing high-value clients consistently</p>
                </div>
                
                <div class="feature-card">
                    <h3>✓ The Service Delivery Mastery System</h3>
                    <p>How to deliver results that make clients beg to pay you more (and refer their friends)</p>
                </div>
                
                <div class="feature-card">
                    <h3>✓ The Scaling Automation Toolkit</h3>
                    <p>Templates, systems, and processes that let you grow without working more hours</p>
                </div>
            </div>
            
            <div class="content-block">
                <div class="highlight">
                    <p><strong>But here's the thing...</strong></p>
                    <p>This isn't for everyone.</p>
                    <p>If you're looking for a "get rich quick" scheme or expect results without putting in the work, this isn't for you.</p>
                    <p>If you're not serious about scaling to $10k-$30k/month and beyond, don't waste my time.</p>
                    <p><strong>But if you're ready to stop playing small and build the agency you've always dreamed of...</strong></p>
                    <p>If you're tired of wondering where your next client will come from...</p>
                    <p>And if you're ready to implement a proven system that actually works in today's market...</p>
                    <p><strong>Then let's talk.</strong></p>
                </div>
            </div>
        </div>
    </section>

    <section class="section">
        <div class="container">
            <h2 class="section-header">"But will this really work for my situation?"</h2>
            
            <div class="faq-item">
                <div class="faq-question">"I'm just starting out - can this work for beginners?"</div>
                <p>Absolutely. This system is designed to take you from zero to your first $10k month, regardless of your current experience level. In fact, beginners often see faster results because they don't have bad habits to unlearn.</p>
            </div>
            
            <div class="faq-item">
                <div class="faq-question">"I've tried other SMMA courses and they didn't work. What makes this different?"</div>
                <p>Simple: I'm not selling you a course. I'm offering to personally walk you through the exact system I use in my own agency. No outdated tactics, no recycled content - just proven strategies that work right now.</p>
            </div>
            
            <div class="faq-item">
                <div class="faq-question">"What if I don't have time to send hundreds of DMs every day?"</div>
                <p>That's exactly why I created this system. The whole point is to automate your outreach and focus your time on high-value activities like sales calls and client delivery.</p>
            </div>
            
            <div class="faq-item">
                <div class="faq-question">"I'm worried about the time commitment. How many hours per week does this require?"</div>
                <p>Once the system is set up, you'll spend most of your time on sales calls and client work - not prospecting. Most of my students find they're working fewer hours than before, but making significantly more money.</p>
            </div>
        </div>
    </section>

    <section class="section">
        <div class="container">
            <div class="guarantee-box">
                <h2 style="color: #ff6b6b; font-size: 2.5rem; margin-bottom: 30px;">Here's my guarantee to you:</h2>
                <p style="font-size: 1.3rem; margin-bottom: 30px;">I'm so confident this system will transform your agency that I'm willing to put my money where my mouth is.</p>
                <p style="font-size: 1.2rem; font-weight: 700; color: #ffd93d;">If you implement everything I show you and don't see measurable progress toward your $10k-$30k/month goal, I'll refund every penny you paid me... PLUS an additional $1,000 for wasting your time.</p>
                <p style="margin-top: 30px; font-size: 1.1rem;">That's how certain I am that this works.</p>
                <p style="color: #ff6b6b; font-weight: 700;">But here's the catch: This guarantee only applies if you actually implement what I teach you.</p>
                <p>I can't help someone who won't help themselves.</p>
            </div>
        </div>
    </section>

    <section class="cta-section">
        <div class="container">
            <h2 style="font-size: 3rem; margin-bottom: 40px; background: linear-gradient(135deg, #ff6b6b 0%, #ffd93d 100%); -webkit-background-clip: text; -webkit-text-fill-color: transparent; background-clip: text;">Ready to finally build the agency you've always wanted?</h2>
            
            <div class="content-block">
                <p style="font-size: 1.3rem; margin-bottom: 30px;">Look, you have two choices right now...</p>
                
                <div style="display: grid; grid-template-columns: repeat(auto-fit, minmax(300px, 1fr)); gap: 40px; margin: 60px 0;">
                    <div style="padding: 40px; border-radius: 20px; background: linear-gradient(135deg, rgba(255, 107, 107, 0.1) 0%, rgba(255, 107, 107, 0.05) 100%); border: 2px solid rgba(255, 107, 107, 0.3);">
                        <h3 style="color: #ff6b6b; font-size: 1.5rem; margin-bottom: 20px;">Choice #1:</h3>
                        <p>Keep doing what you're doing. Keep struggling to find clients. Keep wondering if you'll ever break through to that next level. Keep explaining to people why your "business" isn't making any money yet.</p>
                    </div>
                    
                    <div style="padding: 40px; border-radius: 20px; background: linear-gradient(135deg, rgba(255, 217, 61, 0.1) 0%, rgba(255, 217, 61, 0.05) 100%); border: 2px solid rgba(255, 217, 61, 0.3);">
                        <h3 style="color: #ffd93d; font-size: 1.5rem; margin-bottom: 20px;">Choice #2:</h3>
                        <p>Take action. Book a call. Let me show you exactly how to build a predictable, profitable agency that gives you the freedom and income you started this journey for.</p>
                    </div>
                </div>
                
                <p style="font-size: 1.3rem; margin-bottom: 20px;"><strong>The only question is: Which version of yourself do you want to be six months from now?</strong></p>
                <p style="margin-bottom: 40px;">The one still struggling with the same problems...</p>
                <p style="margin-bottom: 60px;"><strong>Or the one running a thriving $30k/month agency?</strong></p>
                
                <a href="#" class="cta-primary" style="font-size: 1.4rem; padding: 25px 60px;">Book Your Strategy Call Now</a>
                
                <p style="margin-top: 30px; color: #b0b0b0; font-style: italic;">This call is completely free. No obligations. Just a genuine conversation about whether this system is right for you and your goals.</p>
            </div>
        </div>
    </section>

    <script>
        // Add smooth scrolling for better UX
        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function (e) {
                e.preventDefault();
                document.querySelector(this.getAttribute('href')).scrollIntoView({
                    behavior: 'smooth'
                });
            });
        });

        // Add parallax effect to floating elements
        window.addEventListener('scroll', () => {
            const scrolled = window.pageYOffset;
            const parallax = document.querySelectorAll('.floating-element');
            const speed = 0.5;

            parallax.forEach(element => {
                const yPos = -(scrolled * speed);
                element.style.transform = `translate3d(0, ${yPos}px, 0)`;
            });
        });

        // Add entrance animations
        const observerOptions = {
            threshold: 0.1,
            rootMargin: '0px 0px -50px 0px'
        };

        const observer = new IntersectionObserver((entries) => {
            entries.forEach(entry => {
                if (entry.isIntersecting) {
                    entry.target.style.opacity = '1';
                    entry.target.style.transform = 'translateY(0)';
                }
            });
        }, observerOptions);

        // Apply animations to sections
        document.querySelectorAll('.section').forEach(section => {
            section.style.opacity = '0';
            section.style.transform = 'translateY(50px)';
            section.style.transition = 'opacity 0.8s ease, transform 0.8s ease';
            observer.observe(section);
        });
    </script>
</body>
</html>
