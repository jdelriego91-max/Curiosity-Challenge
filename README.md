
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>The Curiosity Challenge</title>
    <style>
        @import url('https://fonts.googleapis.com/css2?family=Inter:wght@400;500;600;700&family=Merriweather:wght@300;400;700&display=swap');
        
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }
        
        body {
            font-family: 'Inter', sans-serif;
            background: linear-gradient(135deg, #f5f7fa 0%, #b4bfca 100%);
            color: #2c3e50;
            min-height: 100vh;
            padding: 20px;
        }
        
        .container {
            max-width: 900px;
            margin: 0 auto;
        }
        
        header {
            text-align: center;
            margin-bottom: 40px;
            position: relative;
        }
        
        .hero-image {
            width: 100%;
            max-width: 900px;
            height: 300px;
            margin: 0 auto 30px;
            border-radius: 20px;
            overflow: hidden;
            position: relative;
            box-shadow: 0 10px 40px rgba(0, 0, 0, 0.1);
        }
        
        .hero-image img {
            width: 100%;
            height: 100%;
            object-fit: cover;
        }
        
        .hero-overlay {
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            bottom: 0;
            background: linear-gradient(to bottom, rgba(245, 247, 250, 0.3), rgba(232, 236, 241, 0.8));
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center;
            padding: 40px;
        }
        
        h1 {
            font-family: 'Merriweather', serif;
            font-size: 3em;
            margin-bottom: 15px;
            color: #577f9d;
            font-weight: 700;
        }
        
        .subtitle {
            font-size: 1.2em;
            color: #34495e;
            line-height: 1.6;
            max-width: 700px;
            margin: 0 auto;
            font-weight: 400;
        }
        
        .practice-section {
            background: white;
            border-radius: 20px;
            padding: 40px;
            margin-bottom: 30px;
            box-shadow: 0 5px 20px rgba(0, 0, 0, 0.08);
        }
        
        .section-title {
            font-family: 'Merriweather', serif;
            font-size: 2em;
            color: #577f9d;
            margin-bottom: 20px;
            font-weight: 700;
        }
        
        .section-subtitle {
            font-size: 1.3em;
            color: #e2b09b;
            margin-bottom: 15px;
            font-weight: 600;
        }
        
        .practice-description {
            font-size: 1.1em;
            line-height: 1.8;
            color: #34495e;
            margin-bottom: 25px;
        }
        
        .curiosity-image {
            width: 100%;
            height: 250px;
            border-radius: 15px;
            overflow: hidden;
            margin: 30px 0;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.1);
        }
        
        .curiosity-image img {
            width: 100%;
            height: 100%;
            object-fit: cover;
        }
        
        .examples-box {
            background: linear-gradient(135deg, #ebf4ff 0%, #b4bfca 100%);
            border-left: 4px solid #577f9d;
            padding: 25px;
            border-radius: 10px;
            margin: 25px 0;
        }
        
        .examples-title {
            font-weight: 600;
            color: #577f9d;
            font-size: 1.1em;
            margin-bottom: 12px;
        }
        
        .examples-list {
            list-style: none;
            padding: 0;
        }
        
        .examples-list li {
            padding: 8px 0;
            color: #34495e;
            font-size: 1em;
            position: relative;
            padding-left: 25px;
        }
        
        .examples-list li:before {
            content: "?";
            position: absolute;
            left: 0;
            color: #e2b09b;
            font-weight: bold;
            font-size: 1.2em;
        }
        
        .steps-container {
            margin: 25px 0;
        }
        
        .step-item {
            display: flex;
            align-items: flex-start;
            margin-bottom: 20px;
            padding: 20px;
            background: #f8f9fa;
            border-radius: 10px;
        }
        
        .step-number {
            background: linear-gradient(135deg, #577f9d, #98a779);
            color: white;
            width: 40px;
            height: 40px;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            font-weight: 700;
            font-size: 1.2em;
            flex-shrink: 0;
            margin-right: 15px;
        }
        
        .step-text {
            color: #34495e;
            font-size: 1.05em;
            line-height: 1.6;
        }
        
        .why-box {
            background: linear-gradient(135deg, #fff4e6 0%, #e2b09b 100%);
            border-left: 4px solid #a85d75;
            padding: 20px;
            border-radius: 10px;
            margin: 20px 0;
        }
        
        .why-box strong {
            color: #a85d75;
        }
        
        .rules-grid {
            display: grid;
            grid-template-columns: 1fr;
            gap: 15px;
            margin: 25px 0;
        }
        
        .rule-card {
            background: white;
            border: 2px solid #577f9d;
            border-radius: 12px;
            padding: 20px;
            display: flex;
            align-items: flex-start;
            gap: 15px;
        }
        
        .rule-number {
            background: #577f9d;
            color: white;
            width: 35px;
            height: 35px;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            font-weight: 700;
            flex-shrink: 0;
        }
        
        .rule-content {
            flex: 1;
        }
        
        .rule-title {
            font-weight: 600;
            color: #577f9d;
            margin-bottom: 5px;
        }
        
        .rule-text {
            color: #34495e;
            font-size: 0.95em;
            line-height: 1.5;
        }
        
        .ptg-grid {
            display: grid;
            grid-template-columns: 1fr;
            gap: 20px;
            margin: 25px 0;
        }
        
        .ptg-card {
            background: white;
            border-radius: 12px;
            padding: 0;
            border: 2px solid #98a779;
            overflow: hidden;
        }
        
        .choice-header {
            background: linear-gradient(135deg, #98a779, #b4bfca);
            color: white;
            padding: 15px 20px;
            font-weight: 600;
            font-size: 1.05em;
        }
        
        .choice-options {
            padding: 20px;
        }
        
        .choice-option {
            display: flex;
            align-items: flex-start;
            gap: 15px;
            padding: 15px;
            margin-bottom: 12px;
            border-radius: 10px;
            cursor: pointer;
            transition: all 0.3s ease;
            background: #f8f9fa;
        }
        
        .choice-option:hover {
            background: #e9ecef;
            transform: translateX(5px);
        }
        
        .choice-option input[type="radio"] {
            margin-top: 3px;
            width: 20px;
            height: 20px;
            cursor: pointer;
            flex-shrink: 0;
            accent-color: #98a779;
        }
        
        .choice-text {
            flex: 1;
            color: #2c3e50;
            line-height: 1.6;
        }
        
        .reflection-intro {
            background: linear-gradient(135deg, #e2b09b 0%, #b4bfca 100%);
            border-left: 4px solid #a85d75;
            padding: 25px;
            border-radius: 10px;
            margin-bottom: 30px;
            color: #2c3e50;
        }
        
        .reflection-intro strong {
            color: #a85d75;
            font-size: 1.1em;
        }
        
        .quick-start-box {
            background: linear-gradient(135deg, #577f9d 0%, #a85d75 100%);
            color: white;
            border-radius: 20px;
            padding: 40px;
            margin: 30px 0;
            text-align: center;
        }
        
        .quick-start-title {
            font-family: 'Merriweather', serif;
            font-size: 2em;
            margin-bottom: 25px;
            font-weight: 700;
        }
        
        .quick-start-steps {
            text-align: left;
            max-width: 600px;
            margin: 0 auto;
        }
        
        .quick-step {
            background: rgba(255, 255, 255, 0.1);
            padding: 15px 20px;
            border-radius: 10px;
            margin-bottom: 15px;
            backdrop-filter: blur(10px);
        }
        
        .quick-step-number {
            font-weight: 700;
            color: #e2b09b;
            margin-right: 10px;
        }
        
        .celebration-text {
            font-size: 1.3em;
            font-weight: 600;
            margin-top: 25px;
            color: #e2b09b;
        }
        
        @media (max-width: 768px) {
            h1 {
                font-size: 2em;
            }
            
            .hero-image {
                height: 200px;
            }
            
            .practice-section {
                padding: 25px;
            }
            
            .section-title {
                font-size: 1.5em;
            }
        }
    </style>
</head>
<body>
    <div class="container">
        <header>
            <div class="hero-image">
                <img src="https://images.unsplash.com/photo-1451187580459-43490279c0fa?w=1200&h=400&fit=crop" alt="Earth from space - curiosity and wonder">
                <div class="hero-overlay">
                    <h1>The Curiosity Challenge</h1>
                    <p class="subtitle">5 Minutes of Wonder Daily</p>
                </div>
            </div>
        </header>
        
        <div class="practice-section">
            <h2 class="section-title">The "Why?" Deep Dive</h2>
            <p class="practice-description">
                A 5-minute daily practice that reignites your natural curiosity and builds a sustainable learning habit through playful exploration. This practice makes learning feel like an adventure rather than a chore, perfect for maintaining the growth mindset you developed at the retreat.
            </p>
            
            <div class="curiosity-image">
                <img src="https://images.unsplash.com/photo-1502134249126-9f3755a50d78?w=1200&h=400&fit=crop" alt="Looking through a magnifying glass">
            </div>
            
            <h3 class="section-subtitle">The Practice</h3>
            <p class="practice-description">
                Pick something you see or use every day but never questioned. Ask "Why?" and spend just 5 minutes discovering the answer.
            </p>
            
            <div class="examples-box">
                <div class="examples-title">Question Examples:</div>
                <ul class="examples-list">
                    <li>Why do we say "bless you" when someone sneezes?</li>
                    <li>Why are stop signs octagonal?</li>
                    <li>Why does coffee smell better than it tastes?</li>
                    <li>Why do we have eyebrows?</li>
                    <li>Why is the sky blue?</li>
                    <li>Why do we shake hands as a greeting?</li>
                </ul>
            </div>
            
            <h3 class="section-subtitle">How It Works</h3>
            <div class="steps-container">
                <div class="step-item">
                    <div class="step-number">1</div>
                    <div class="step-text">Ask your question out loud (seriously, say it)</div>
                </div>
                
                <div class="step-item">
                    <div class="step-number">2</div>
                    <div class="step-text">Spend 3 minutes finding the answer (Wikipedia, Google, YouTube)</div>
                </div>
                
                <div class="step-item">
                    <div class="step-number">3</div>
                    <div class="step-text">Tell someone what you learned OR write it down in one sentence</div>
                </div>
            </div>
            
            <div class="why-box">
                <strong>Why it works:</strong> Following your genuine curiosity activates dopamine pathways—the same feeling kids get when they discover something cool. Learning becomes a reward, not a task.
            </div>
        </div>
        
        <div class="practice-section">
            <h2 class="section-title">The Golden Rules</h2>
            
            <div class="rules-grid">
                <div class="rule-card">
                    <div class="rule-number">1</div>
                    <div class="rule-content">
                        <div class="rule-title">Follow Genuine Interest</div>
                        <div class="rule-text">If it doesn't spark curiosity, pick something else</div>
                    </div>
                </div>
                
                <div class="rule-card">
                    <div class="rule-number">2</div>
                    <div class="rule-content">
                        <div class="rule-title">No Judgment Zone</div>
                        <div class="rule-text">Learning about Pokemon is as valid as learning about philosophy</div>
                    </div>
                </div>
                
                <div class="rule-card">
                    <div class="rule-number">3</div>
                    <div class="rule-content">
                        <div class="rule-title">Imperfect Action</div>
                        <div class="rule-text">5 scattered minutes beats 0 perfect minutes</div>
                    </div>
                </div>
                
                <div class="rule-card">
                    <div class="rule-number">4</div>
                    <div class="rule-content">
                        <div class="rule-title">Share Discoveries</div>
                        <div class="rule-text">Tell at least one person per week what you learned</div>
                    </div>
                </div>
                
                <div class="rule-card">
                    <div class="rule-number">5</div>
                    <div class="rule-content">
                        <div class="rule-title">Celebrate Trying</div>
                        <div class="rule-text">The goal is curiosity, not mastery</div>
                    </div>
                </div>
            </div>
        </div>
        
        <div class="practice-section">
            <h2 class="section-title">Reflection: Where Are You Now?</h2>
            
            <div class="reflection-intro">
                <strong>Curiosity Assessment:</strong> Choose the response that feels more true for you right now, even if both have some truth. There are no right or wrong answers—this is about honest self-reflection.
            </div>
            
            <div class="ptg-grid">
                <div class="ptg-card">
                    <div class="choice-header">When I encounter something I don't understand...</div>
                    <div class="choice-options">
                        <label class="choice-option">
                            <input type="radio" name="q1" value="a">
                            <span class="choice-text">I feel frustrated and want to avoid it</span>
                        </label>
                        <label class="choice-option">
                            <input type="radio" name="q1" value="b">
                            <span class="choice-text">I feel curious and want to figure it out</span>
                        </label>
                    </div>
                </div>
                
                <div class="ptg-card">
                    <div class="choice-header">When I think about learning something new...</div>
                    <div class="choice-options">
                        <label class="choice-option">
                            <input type="radio" name="q2" value="a">
                            <span class="choice-text">I worry about whether I'll be good at it</span>
                        </label>
                        <label class="choice-option">
                            <input type="radio" name="q2" value="b">
                            <span class="choice-text">I get excited about what I might discover</span>
                        </label>
                    </div>
                </div>
                
                <div class="ptg-card">
                    <div class="choice-header">My relationship with asking questions is...</div>
                    <div class="choice-options">
                        <label class="choice-option">
                            <input type="radio" name="q3" value="a">
                            <span class="choice-text">I hold back because I don't want to look uninformed</span>
                        </label>
                        <label class="choice-option">
                            <input type="radio" name="q3" value="b">
                            <span class="choice-text">I freely ask because curiosity matters more than appearance</span>
                        </label>
                    </div>
                </div>
                
                <div class="ptg-card">
                    <div class="choice-header">When I make a mistake while learning...</div>
                    <div class="choice-options">
                        <label class="choice-option">
                            <input type="radio" name="q4" value="a">
                            <span class="choice-text">I see it as proof I'm not capable</span>
                        </label>
                        <label class="choice-option">
                            <input type="radio" name="q4" value="b">
                            <span class="choice-text">I see it as useful feedback for growth</span>
                        </label>
                    </div>
                </div>
                
                <div class="ptg-card">
                    <div class="choice-header">My current belief about my capacity to grow is...</div>
                    <div class="choice-options">
                        <label class="choice-option">
                            <input type="radio" name="q5" value="a">
                            <span class="choice-text">I'm pretty much who I am, change is hard</span>
                        </label>
                        <label class="choice-option">
                            <input type="radio" name="q5" value="b">
                            <span class="choice-text">I can develop new capacities with effort and practice</span>
                        </label>
                    </div>
                </div>
                
                <div class="ptg-card">
                    <div class="choice-header">When others know more than me about something...</div>
                    <div class="choice-options">
                        <label class="choice-option">
                            <input type="radio" name="q6" value="a">
                            <span class="choice-text">I feel intimidated or less-than</span>
                        </label>
                        <label class="choice-option">
                            <input type="radio" name="q6" value="b">
                            <span class="choice-text">I see an opportunity to learn from them</span>
                        </label>
                    </div>
                </div>
            </div>
            
            <div class="reflection-intro" style="margin-top: 30px;">
                <strong>Reflection:</strong> Notice which responses felt more true. The "b" responses reflect a growth mindset and active curiosity. If you chose mostly "a" responses, that's valuable information—it shows where building curiosity practices could have the biggest impact on your continued growth.
            </div>
        </div>
        
        <div class="quick-start-box">
            <h2 class="quick-start-title">Quick Start Guide</h2>
            
            <div class="quick-start-steps">
                <div class="quick-step">
                    <span class="quick-step-number">Right Now:</span>
                    Set a daily 5-minute phone reminder: "Curiosity Challenge"
                </div>
                
                <div class="quick-step">
                    <span class="quick-step-number">Today:</span>
                    Pick one thing you're mildly curious about
                </div>
                
                <div class="quick-step">
                    <span class="quick-step-number">Next 5 Minutes:</span>
                    Spend 5 minutes exploring it
                </div>
                
                <div class="quick-step">
                    <span class="quick-step-number">Before Bed:</span>
                    Tell someone what you learned
                </div>
            </div>
            
            <p class="celebration-text">That's it. You just completed day 1.</p>
            
            <p style="margin-top: 30px; font-size: 1.1em; line-height: 1.6;">
                The best learners aren't the smartest—they're the most curious. This practice rebuilds that childlike wonder that makes learning effortless and fun.
            </p>
        </div>
    </div>
</body>
</html>
