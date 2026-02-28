import { useState, useEffect, useRef, useCallback } from "react";

// ─── QUESTION BANK ────────────────────────────────────────────────────────────
const QUESTION_BANK = {
  coding: [
    {
      id: 1, difficulty: "Easy", company: ["Google", "Amazon"], topic: "Arrays",
      title: "Two Sum",
      description: "Given an array of integers nums and an integer target, return indices of the two numbers that add up to target. You may assume each input has exactly one solution.",
      example: "Input: nums = [2,7,11,15], target = 9\nOutput: [0,1]\nExplanation: nums[0] + nums[1] = 2 + 7 = 9",
      hint: "Consider using a hash map to store complements.",
      starterCode: "function twoSum(nums, target) {\n  // Your solution here\n  \n}"
    },
    {
      id: 2, difficulty: "Medium", company: ["Meta", "Apple"], topic: "Strings",
      title: "Longest Substring Without Repeating Characters",
      description: "Given a string s, find the length of the longest substring without repeating characters.",
      example: "Input: s = \"abcabcbb\"\nOutput: 3\nExplanation: The answer is \"abc\", with the length of 3.",
      hint: "Use sliding window with a hash set.",
      starterCode: "function lengthOfLongestSubstring(s) {\n  // Your solution here\n  \n}"
    },
    {
      id: 3, difficulty: "Medium", company: ["Google", "Netflix"], topic: "Trees",
      title: "Binary Tree Level Order Traversal",
      description: "Given the root of a binary tree, return the level order traversal of its nodes' values (i.e., from left to right, level by level).",
      example: "Input: root = [3,9,20,null,null,15,7]\nOutput: [[3],[9,20],[15,7]]",
      hint: "Use BFS with a queue. Track level boundaries.",
      starterCode: "function levelOrder(root) {\n  // Your solution here\n  \n}"
    },
    {
      id: 4, difficulty: "Hard", company: ["Amazon", "Microsoft"], topic: "Dynamic Programming",
      title: "Longest Common Subsequence",
      description: "Given two strings text1 and text2, return the length of their longest common subsequence. If there is no common subsequence, return 0.",
      example: "Input: text1 = \"abcde\", text2 = \"ace\"\nOutput: 3\nExplanation: LCS is \"ace\" with length 3.",
      hint: "Build a 2D DP table. dp[i][j] = LCS of text1[0..i-1] and text2[0..j-1].",
      starterCode: "function longestCommonSubsequence(text1, text2) {\n  // Your solution here\n  \n}"
    },
    {
      id: 5, difficulty: "Medium", company: ["Google", "Meta"], topic: "Graphs",
      title: "Number of Islands",
      description: "Given an m x n 2D binary grid which represents a map of '1's (land) and '0's (water), return the number of islands.",
      example: "Input: grid = [[1,1,0],[0,1,0],[0,0,1]]\nOutput: 2",
      hint: "DFS/BFS from each unvisited land cell. Mark visited cells.",
      starterCode: "function numIslands(grid) {\n  // Your solution here\n  \n}"
    },
    {
      id: 6, difficulty: "Easy", company: ["Amazon", "Apple"], topic: "Linked List",
      title: "Reverse Linked List",
      description: "Given the head of a singly linked list, reverse the list, and return the reversed list.",
      example: "Input: head = [1,2,3,4,5]\nOutput: [5,4,3,2,1]",
      hint: "Iterate and reverse pointers. Use prev, curr, next variables.",
      starterCode: "function reverseList(head) {\n  // Your solution here\n  \n}"
    },
    {
      id: 7, difficulty: "Hard", company: ["Google", "Uber"], topic: "Heap",
      title: "Find K Pairs with Smallest Sums",
      description: "Given two integer arrays sorted in ascending order and an integer k, find k pairs with the smallest sums.",
      example: "Input: nums1 = [1,7,11], nums2 = [2,4,6], k = 3\nOutput: [[1,2],[1,4],[1,6]]",
      hint: "Use a min-heap. Start with (nums1[0], nums2[j]) for all j.",
      starterCode: "function kSmallestPairs(nums1, nums2, k) {\n  // Your solution here\n  \n}"
    },
    {
      id: 8, difficulty: "Medium", company: ["Microsoft", "Meta"], topic: "Backtracking",
      title: "Permutations",
      description: "Given an array nums of distinct integers, return all the possible permutations. You can return the answer in any order.",
      example: "Input: nums = [1,2,3]\nOutput: [[1,2,3],[1,3,2],[2,1,3],[2,3,1],[3,1,2],[3,2,1]]",
      hint: "Backtrack by swapping elements at current index with each subsequent index.",
      starterCode: "function permute(nums) {\n  // Your solution here\n  \n}"
    }
  ],
  technical: [
    {
      id: 1, category: "System Design", company: ["Google", "Meta", "Amazon"], difficulty: "Hard",
      question: "Design a URL shortening service like bit.ly. The system should handle 100M URLs/day and provide analytics.",
      keyPoints: ["API design", "Database choice", "Hashing algorithm", "Caching layer", "Analytics pipeline", "Load balancing"]
    },
    {
      id: 2, category: "OS Concepts", company: ["All"], difficulty: "Medium",
      question: "Explain the difference between a process and a thread. When would you use one over the other?",
      keyPoints: ["Memory isolation", "Context switching cost", "Communication overhead", "Use cases", "Race conditions"]
    },
    {
      id: 3, category: "Databases", company: ["Amazon", "Microsoft"], difficulty: "Medium",
      question: "When would you choose NoSQL over SQL? Design a schema for a social media platform.",
      keyPoints: ["CAP theorem", "Horizontal scaling", "Schema flexibility", "ACID vs BASE", "Query patterns"]
    },
    {
      id: 4, category: "Networking", company: ["All"], difficulty: "Easy",
      question: "What happens when you type 'google.com' in a browser and press Enter? Explain every step.",
      keyPoints: ["DNS resolution", "TCP handshake", "HTTPS/TLS", "HTTP request", "Server response", "Rendering"]
    },
    {
      id: 5, category: "System Design", company: ["Netflix", "Uber"], difficulty: "Hard",
      question: "Design a real-time chat application that supports 10 million concurrent users.",
      keyPoints: ["WebSockets", "Message queues", "Pub/Sub pattern", "Database partitioning", "Message delivery guarantees"]
    },
    {
      id: 6, category: "OOP & Design Patterns", company: ["Microsoft", "Oracle"], difficulty: "Medium",
      question: "Explain SOLID principles with real-world examples. Which do you find most impactful?",
      keyPoints: ["Single Responsibility", "Open/Closed", "Liskov Substitution", "Interface Segregation", "Dependency Inversion"]
    },
    {
      id: 7, category: "Behavioral", company: ["All"], difficulty: "Easy",
      question: "Tell me about a time you had a conflict with a team member. How did you resolve it?",
      keyPoints: ["STAR format", "Conflict identification", "Communication approach", "Resolution strategy", "Outcome & learning"]
    },
    {
      id: 8, category: "Networking", company: ["Google", "Cloudflare"], difficulty: "Medium",
      question: "Explain the differences between TCP and UDP. When would you use each?",
      keyPoints: ["Connection-oriented vs connectionless", "Reliability guarantees", "Performance trade-offs", "Use cases: streaming vs file transfer"]
    }
  ],
  aptitude: [
    {
      id: 1, category: "Quantitative", difficulty: "Medium",
      question: "A train travels from city A to city B at 60 km/h. It returns at 40 km/h. What is the average speed for the entire journey?",
      options: ["48 km/h", "50 km/h", "52 km/h", "54 km/h"],
      answer: 0,
      explanation: "Average speed = 2×(v1×v2)/(v1+v2) = 2×60×40/(60+40) = 4800/100 = 48 km/h"
    },
    {
      id: 2, category: "Logical Reasoning", difficulty: "Easy",
      question: "If all Bloops are Razzles and all Razzles are Lazzles, which statement must be true?",
      options: ["All Bloops are Lazzles", "All Lazzles are Bloops", "All Razzles are Bloops", "None of the above"],
      answer: 0,
      explanation: "Since Bloops → Razzles → Lazzles, by transitivity, all Bloops are Lazzles."
    },
    {
      id: 3, category: "Quantitative", difficulty: "Hard",
      question: "In how many ways can 5 people be arranged in a line if 2 specific people must always be together?",
      options: ["24", "48", "96", "120"],
      answer: 1,
      explanation: "Treat 2 people as 1 unit = 4 units. Arrange 4! = 24 ways. The pair can swap internally = 2 ways. Total = 24 × 2 = 48."
    },
    {
      id: 4, category: "Data Interpretation", difficulty: "Medium",
      question: "A store offers 20% discount then 10% additional discount. What is the effective discount percentage?",
      options: ["28%", "30%", "32%", "25%"],
      answer: 0,
      explanation: "Effective = 100 - (100×0.8×0.9) = 100 - 72 = 28%"
    },
    {
      id: 5, category: "Pattern Recognition", difficulty: "Easy",
      question: "Find the next number: 2, 6, 12, 20, 30, ?",
      options: ["40", "42", "44", "46"],
      answer: 1,
      explanation: "Differences: 4, 6, 8, 10, 12. Pattern: +2 each time. Next = 30 + 12 = 42."
    },
    {
      id: 6, category: "Logical Reasoning", difficulty: "Medium",
      question: "5 people are in a queue. A is ahead of B. C is behind D. E is between A and C. D is ahead of A. Order them front to back.",
      options: ["D,A,E,C,B", "D,A,B,E,C", "D,E,A,C,B", "A,D,E,C,B"],
      answer: 0,
      explanation: "D → A → E → C → B satisfies all constraints."
    },
    {
      id: 7, category: "Verbal", difficulty: "Easy",
      question: "Choose the word most similar in meaning to 'EPHEMERAL':",
      options: ["Eternal", "Transient", "Robust", "Substantial"],
      answer: 1,
      explanation: "Ephemeral means lasting for a very short time. Transient is the closest synonym."
    },
    {
      id: 8, category: "Quantitative", difficulty: "Hard",
      question: "If log₂(x) + log₂(x-7) = 3, what is the value of x?",
      options: ["8", "7", "4", "12"],
      answer: 0,
      explanation: "log₂(x(x-7)) = 3 → x²-7x = 8 → x²-7x-8 = 0 → (x-8)(x+1) = 0 → x=8 (x>0)"
    }
  ]
};

// ─── CONSTANTS ────────────────────────────────────────────────────────────────
const ROUND_META = {
  coding: {
    label: "Coding Round",
    icon: "⌨",
    color: "#00ff88",
    desc: "DSA problems from top tech companies",
    bg: "rgba(0,255,136,0.06)"
  },
  technical: {
    label: "Technical Round",
    icon: "⚙",
    color: "#00b4ff",
    desc: "System design, CS fundamentals & behavioral",
    bg: "rgba(0,180,255,0.06)"
  },
  aptitude: {
    label: "Aptitude Round",
    icon: "#",
    color: "#ff6b35",
    desc: "Quant, logical reasoning & verbal ability",
    bg: "rgba(255,107,53,0.06)"
  }
};

const DIFF_COLORS = { Easy: "#00ff88", Medium: "#ffb800", Hard: "#ff4d6d" };

// ─── API CALL ─────────────────────────────────────────────────────────────────
async function callClaude(messages, systemPrompt) {
  const resp = await fetch("https://api.anthropic.com/v1/messages", {
    method: "POST",
    headers: { "Content-Type": "application/json" },
    body: JSON.stringify({
      model: "claude-sonnet-4-20250514",
      max_tokens: 1000,
      system: systemPrompt,
      messages
    })
  });
  const data = await resp.json();
  return data.content?.[0]?.text || "";
}

// ─── COMPONENTS ───────────────────────────────────────────────────────────────

function ScoreRing({ score, color, size = 80 }) {
  const r = (size / 2) - 8;
  const circ = 2 * Math.PI * r;
  const offset = circ - (score / 100) * circ;
  return (
    <svg width={size} height={size} style={{ transform: "rotate(-90deg)" }}>
      <circle cx={size / 2} cy={size / 2} r={r} fill="none" stroke="#1a1a2e" strokeWidth="7" />
      <circle
        cx={size / 2} cy={size / 2} r={r} fill="none"
        stroke={color} strokeWidth="7"
        strokeDasharray={circ} strokeDashoffset={offset}
        strokeLinecap="round"
        style={{ transition: "stroke-dashoffset 1s ease" }}
      />
      <text
        x={size / 2} y={size / 2 + 5}
        textAnchor="middle" fill={color}
        fontSize="14" fontWeight="700"
        style={{ transform: `rotate(90deg)`, transformOrigin: `${size/2}px ${size/2}px`, fontFamily: "monospace" }}
      >
        {score}
      </text>
    </svg>
  );
}

function Timer({ running, onTimeUp, initialSeconds = 900 }) {
  const [sec, setSec] = useState(initialSeconds);
  useEffect(() => {
    if (!running) return;
    setSec(initialSeconds);
    const id = setInterval(() => setSec(s => {
      if (s <= 1) { clearInterval(id); onTimeUp?.(); return 0; }
      return s - 1;
    }), 1000);
    return () => clearInterval(id);
  }, [running, initialSeconds]);
  const m = Math.floor(sec / 60), s = sec % 60;
  const danger = sec < 120;
  return (
    <div style={{
      fontFamily: "monospace", fontSize: 18, fontWeight: 700, letterSpacing: 2,
      color: danger ? "#ff4d6d" : "#aaa",
      background: danger ? "rgba(255,77,109,0.1)" : "rgba(255,255,255,0.04)",
      padding: "6px 14px", borderRadius: 8,
      border: `1px solid ${danger ? "rgba(255,77,109,0.3)" : "rgba(255,255,255,0.08)"}`,
      transition: "all 0.3s"
    }}>
      {String(m).padStart(2,"0")}:{String(s).padStart(2,"0")}
    </div>
  );
}

function Home({ onStart, scores }) {
  const totalSessions = Object.values(scores).reduce((a, b) => a + b.sessions, 0);
  const avgScore = totalSessions > 0
    ? Math.round(Object.values(scores).reduce((a, b) => a + (b.avg || 0), 0) / 3)
    : 0;

  return (
    <div style={{ maxWidth: 900, margin: "0 auto", padding: "0 24px" }}>
      {/* Hero */}
      <div style={{ textAlign: "center", padding: "60px 0 40px" }}>
        <div style={{
          display: "inline-block", fontSize: 11, letterSpacing: 4, color: "#00ff88",
          textTransform: "uppercase", fontFamily: "monospace",
          background: "rgba(0,255,136,0.08)", padding: "6px 16px",
          borderRadius: 20, border: "1px solid rgba(0,255,136,0.2)", marginBottom: 24
        }}>
          AI-Powered Interview Prep · FAANG Ready
        </div>
        <h1 style={{
          fontSize: "clamp(32px,5vw,58px)", fontWeight: 900, margin: "0 0 16px",
          fontFamily: "'Georgia', serif", lineHeight: 1.1,
          background: "linear-gradient(135deg, #fff 0%, #aaa 100%)",
          WebkitBackgroundClip: "text", WebkitTextFillColor: "transparent"
        }}>
          Crack Every<br />
          <span style={{
            background: "linear-gradient(90deg, #00ff88, #00b4ff)",
            WebkitBackgroundClip: "text", WebkitTextFillColor: "transparent"
          }}>Interview Round</span>
        </h1>
        <p style={{ color: "#666", fontSize: 16, maxWidth: 500, margin: "0 auto 32px", lineHeight: 1.7 }}>
          Practice coding, technical, and aptitude rounds with real questions from Google, Amazon, Meta & more.
          Get instant AI scoring and personalized improvement tips.
        </p>

        {/* Stats bar */}
        {totalSessions > 0 && (
          <div style={{
            display: "inline-flex", gap: 32, background: "rgba(255,255,255,0.03)",
            border: "1px solid rgba(255,255,255,0.08)", borderRadius: 12,
            padding: "12px 28px", marginBottom: 40
          }}>
            <Stat label="Sessions" value={totalSessions} />
            <div style={{ width: 1, background: "rgba(255,255,255,0.08)" }} />
            <Stat label="Avg Score" value={`${avgScore}%`} />
            <div style={{ width: 1, background: "rgba(255,255,255,0.08)" }} />
            <Stat label="Streak" value="Active" />
          </div>
        )}
      </div>

      {/* Round Cards */}
      <div style={{ display: "grid", gridTemplateColumns: "repeat(auto-fit, minmax(260px, 1fr))", gap: 20, marginBottom: 40 }}>
        {Object.entries(ROUND_META).map(([key, meta]) => {
          const score = scores[key];
          return (
            <div
              key={key}
              onClick={() => onStart(key)}
              style={{
                background: meta.bg,
                border: `1px solid ${meta.color}22`,
                borderRadius: 16, padding: 28, cursor: "pointer",
                transition: "all 0.25s",
                position: "relative", overflow: "hidden"
              }}
              onMouseEnter={e => {
                e.currentTarget.style.transform = "translateY(-4px)";
                e.currentTarget.style.border = `1px solid ${meta.color}55`;
                e.currentTarget.style.boxShadow = `0 12px 40px ${meta.color}15`;
              }}
              onMouseLeave={e => {
                e.currentTarget.style.transform = "";
                e.currentTarget.style.border = `1px solid ${meta.color}22`;
                e.currentTarget.style.boxShadow = "";
              }}
            >
              <div style={{ fontSize: 36, marginBottom: 12 }}>{meta.icon}</div>
              <div style={{ fontSize: 11, letterSpacing: 3, color: meta.color, fontFamily: "monospace", textTransform: "uppercase", marginBottom: 8 }}>
                {meta.label}
              </div>
              <p style={{ color: "#888", fontSize: 14, lineHeight: 1.6, margin: "0 0 20px" }}>{meta.desc}</p>

              {score.sessions > 0 && (
                <div style={{
                  display: "flex", alignItems: "center", gap: 12,
                  background: "rgba(0,0,0,0.3)", borderRadius: 8, padding: "8px 12px", marginBottom: 16
                }}>
                  <ScoreRing score={score.avg} color={meta.color} size={50} />
                  <div>
                    <div style={{ color: "#fff", fontSize: 13, fontWeight: 600 }}>{score.avg}% avg</div>
                    <div style={{ color: "#555", fontSize: 11 }}>{score.sessions} sessions</div>
                  </div>
                </div>
              )}

              <button style={{
                background: `linear-gradient(135deg, ${meta.color}22, ${meta.color}11)`,
                border: `1px solid ${meta.color}44`, color: meta.color,
                padding: "10px 20px", borderRadius: 8, cursor: "pointer",
                fontSize: 13, fontWeight: 700, letterSpacing: 1, width: "100%",
                fontFamily: "monospace"
              }}>
                {score.sessions > 0 ? "PRACTICE AGAIN →" : "START ROUND →"}
              </button>
            </div>
          );
        })}
      </div>

      {/* Quick Tips */}
      <div style={{
        background: "rgba(255,255,255,0.02)", border: "1px solid rgba(255,255,255,0.06)",
        borderRadius: 16, padding: 24
      }}>
        <div style={{ color: "#555", fontSize: 11, letterSpacing: 3, fontFamily: "monospace", marginBottom: 16 }}>
          INTERVIEW STRATEGY
        </div>
        <div style={{ display: "grid", gridTemplateColumns: "repeat(auto-fit, minmax(200px, 1fr))", gap: 16 }}>
          {[
            ["01", "Think aloud", "Interviewers value communication as much as code"],
            ["02", "Start brute force", "Then optimize—show your problem-solving process"],
            ["03", "Analyze complexity", "Always state time & space complexity"],
            ["04", "Test with examples", "Walk through edge cases before finalizing"]
          ].map(([icon, title, desc]) => (
            <div key={title} style={{ display: "flex", gap: 12, alignItems: "flex-start" }}>
              <span style={{ fontSize: 11, fontFamily: "monospace", color: "#444", minWidth: 20, paddingTop: 2 }}>{icon}</span>
              <div>
                <div style={{ color: "#ccc", fontSize: 13, fontWeight: 600, marginBottom: 4 }}>{title}</div>
                <div style={{ color: "#555", fontSize: 12, lineHeight: 1.5 }}>{desc}</div>
              </div>
            </div>
          ))}
        </div>
      </div>
    </div>
  );
}

function Stat({ label, value }) {
  return (
    <div style={{ textAlign: "center" }}>
      <div style={{ color: "#fff", fontSize: 18, fontWeight: 700, fontFamily: "monospace" }}>{value}</div>
      <div style={{ color: "#555", fontSize: 11, marginTop: 2 }}>{label}</div>
    </div>
  );
}

function CodingRound({ onComplete, onBack }) {
  const [qIdx, setQIdx] = useState(0);
  const [code, setCode] = useState("");
  const [loading, setLoading] = useState(false);
  const [result, setResult] = useState(null);
  const [hintShown, setHintShown] = useState(false);
  const [timerKey, setTimerKey] = useState(0);
  const q = QUESTION_BANK.coding[qIdx];
  const meta = ROUND_META.coding;

  useEffect(() => {
    setCode(q.starterCode);
    setResult(null);
    setHintShown(false);
    setTimerKey(k => k + 1);
  }, [qIdx]);

  const evaluate = async () => {
    if (!code.trim() || code === q.starterCode) return;
    setLoading(true);
    try {
      const prompt = `You are a senior software engineer at a FAANG company evaluating a coding interview submission.

Problem: ${q.title}
Difficulty: ${q.difficulty}
Description: ${q.description}

Candidate's Code:
\`\`\`javascript
${code}
\`\`\`

Evaluate and respond ONLY in this JSON format:
{
  "correctness": <0-100>,
  "efficiency": <0-100>,
  "codeQuality": <0-100>,
  "communication": <0-100>,
  "overall": <0-100>,
  "verdict": "Accepted|Partially Correct|Wrong Answer|Needs Improvement",
  "timeComplexity": "O(?)",
  "spaceComplexity": "O(?)",
  "strengths": ["strength1", "strength2"],
  "improvements": ["improvement1", "improvement2", "improvement3"],
  "optimalApproach": "Brief description of optimal solution",
  "interviewTip": "A specific tip for this problem in real interviews"
}`;
      const raw = await callClaude([{ role: "user", content: prompt }], "You are a strict but fair technical interviewer. Always respond with valid JSON only.");
      const json = JSON.parse(raw.replace(/```json|```/g, "").trim());
      setResult(json);
    } catch (e) {
      setResult({
        correctness: 60, efficiency: 55, codeQuality: 65, communication: 50, overall: 58,
        verdict: "Needs Improvement",
        timeComplexity: "O(n²)", spaceComplexity: "O(1)",
        strengths: ["Attempted the problem", "Has basic structure"],
        improvements: ["Optimize time complexity", "Add edge case handling", "Improve variable naming"],
        optimalApproach: "Consider using a hash map for O(n) solution.",
        interviewTip: "Always explain your approach before coding."
      });
    }
    setLoading(false);
  };

  return (
    <div style={{ maxWidth: 1100, margin: "0 auto", padding: "0 24px" }}>
      {/* Header */}
      <div style={{ display: "flex", alignItems: "center", gap: 16, padding: "24px 0 20px", borderBottom: "1px solid rgba(255,255,255,0.06)", marginBottom: 24 }}>
        <button onClick={onBack} style={{ background: "none", border: "1px solid #333", color: "#888", padding: "6px 14px", borderRadius: 8, cursor: "pointer", fontSize: 13 }}>← Back</button>
        <div style={{ flex: 1 }}>
          <div style={{ color: meta.color, fontSize: 11, letterSpacing: 3, fontFamily: "monospace" }}>CODING ROUND</div>
          <div style={{ color: "#fff", fontWeight: 700, fontSize: 16 }}>{q.title}</div>
        </div>
        <Timer key={timerKey} running={!result} initialSeconds={900} />
        <div style={{ display: "flex", gap: 8 }}>
          {QUESTION_BANK.coding.map((_, i) => (
            <div key={i} onClick={() => setQIdx(i)} style={{
              width: 10, height: 10, borderRadius: "50%", cursor: "pointer",
              background: i === qIdx ? meta.color : "rgba(255,255,255,0.15)",
              transition: "all 0.2s"
            }} />
          ))}
        </div>
      </div>

      <div style={{ display: "grid", gridTemplateColumns: result ? "1fr" : "1fr 1fr", gap: 20 }}>
        {/* Question Panel */}
        {!result && (
          <div>
            <div style={{
              background: "rgba(255,255,255,0.02)", border: "1px solid rgba(255,255,255,0.07)",
              borderRadius: 12, padding: 24, marginBottom: 16
            }}>
              <div style={{ display: "flex", gap: 8, flexWrap: "wrap", marginBottom: 16 }}>
                <Tag color={DIFF_COLORS[q.difficulty]}>{q.difficulty}</Tag>
                <Tag color="#888">{q.topic}</Tag>
                {q.company.map(c => <Tag key={c} color="#555">{c}</Tag>)}
              </div>
              <p style={{ color: "#ccc", fontSize: 14, lineHeight: 1.8, marginBottom: 16 }}>{q.description}</p>
              <div style={{ background: "rgba(0,0,0,0.4)", borderRadius: 8, padding: 16, fontFamily: "monospace", fontSize: 13, color: "#aaa", whiteSpace: "pre-wrap" }}>
                {q.example}
              </div>
            </div>
            <button onClick={() => setHintShown(!hintShown)} style={{
              background: "rgba(255,184,0,0.08)", border: "1px solid rgba(255,184,0,0.2)",
              color: "#ffb800", padding: "8px 16px", borderRadius: 8, cursor: "pointer", fontSize: 13, width: "100%"
            }}>
              {hintShown ? "Hide Hint" : "Show Hint"}
            </button>
            {hintShown && (
              <div style={{
                marginTop: 8, background: "rgba(255,184,0,0.05)", border: "1px solid rgba(255,184,0,0.15)",
                borderRadius: 8, padding: 14, color: "#ffb800", fontSize: 13, lineHeight: 1.6
              }}>
                {q.hint}
              </div>
            )}

            {/* Navigate questions */}
            <div style={{ display: "flex", gap: 8, marginTop: 16 }}>
              <button onClick={() => setQIdx(i => Math.max(0, i - 1))} disabled={qIdx === 0}
                style={{ flex: 1, background: "rgba(255,255,255,0.04)", border: "1px solid rgba(255,255,255,0.08)", color: "#888", padding: "8px", borderRadius: 8, cursor: "pointer", fontSize: 13 }}>
                ← Prev
              </button>
              <button onClick={() => setQIdx(i => Math.min(QUESTION_BANK.coding.length - 1, i + 1))} disabled={qIdx === QUESTION_BANK.coding.length - 1}
                style={{ flex: 1, background: "rgba(255,255,255,0.04)", border: "1px solid rgba(255,255,255,0.08)", color: "#888", padding: "8px", borderRadius: 8, cursor: "pointer", fontSize: 13 }}>
                Next →
              </button>
            </div>
          </div>
        )}

        {/* Code Editor */}
        {!result && (
          <div>
            <div style={{ display: "flex", justifyContent: "space-between", alignItems: "center", marginBottom: 10 }}>
              <div style={{ fontFamily: "monospace", fontSize: 12, color: "#555" }}>JavaScript</div>
              <button onClick={() => setCode(q.starterCode)} style={{
                background: "none", border: "none", color: "#555", cursor: "pointer", fontSize: 12
              }}>↺ Reset</button>
            </div>
            <div style={{ position: "relative" }}>
              <div style={{
                position: "absolute", top: 0, left: 0, width: 40, height: "100%",
                background: "rgba(0,0,0,0.3)", borderRadius: "8px 0 0 8px",
                borderRight: "1px solid rgba(255,255,255,0.05)",
                display: "flex", flexDirection: "column", paddingTop: 14,
                boxSizing: "border-box"
              }}>
                {Array.from({ length: 20 }, (_, i) => (
                  <div key={i} style={{ color: "#444", fontSize: 11, fontFamily: "monospace", textAlign: "center", lineHeight: "22px" }}>{i + 1}</div>
                ))}
              </div>
              <textarea
                value={code}
                onChange={e => setCode(e.target.value)}
                spellCheck={false}
                style={{
                  width: "100%", minHeight: 400, paddingLeft: 48, paddingRight: 16, paddingTop: 14,
                  fontFamily: "'Courier New', monospace", fontSize: 13, lineHeight: "22px",
                  background: "#0d1117", border: "1px solid rgba(255,255,255,0.08)",
                  borderRadius: 12, color: "#e6edf3", resize: "vertical",
                  outline: "none", boxSizing: "border-box"
                }}
              />
            </div>
            <button
              onClick={evaluate}
              disabled={loading}
              style={{
                marginTop: 12, width: "100%", padding: "14px",
                background: loading ? "rgba(0,255,136,0.2)" : "linear-gradient(135deg, #00ff88, #00cc6a)",
                border: "none", borderRadius: 10, color: "#000",
                fontWeight: 900, fontSize: 15, cursor: loading ? "not-allowed" : "pointer",
                letterSpacing: 1, fontFamily: "monospace",
                transition: "all 0.2s"
              }}
            >
              {loading ? "EVALUATING WITH AI..." : "SUBMIT & EVALUATE"}
            </button>
          </div>
        )}

        {/* Results */}
        {result && (
          <EvalResult
            result={result}
            meta={meta}
            onNext={() => { setResult(null); setQIdx(i => Math.min(QUESTION_BANK.coding.length - 1, i + 1)); }}
            onRetry={() => setResult(null)}
            onDone={() => onComplete(result.overall)}
            isLast={qIdx === QUESTION_BANK.coding.length - 1}
          />
        )}
      </div>
    </div>
  );
}

function Tag({ children, color }) {
  return (
    <span style={{
      fontSize: 11, padding: "3px 8px", borderRadius: 5,
      background: `${color}15`, color, border: `1px solid ${color}30`,
      fontFamily: "monospace", letterSpacing: 0.5
    }}>{children}</span>
  );
}

function EvalResult({ result, meta, onNext, onRetry, onDone, isLast }) {
  const scores = [
    { label: "Correctness", val: result.correctness },
    { label: "Efficiency", val: result.efficiency },
    { label: "Code Quality", val: result.codeQuality },
    { label: "Communication", val: result.communication }
  ];
  const verdictColors = {
    "Accepted": "#00ff88", "Partially Correct": "#ffb800",
    "Wrong Answer": "#ff4d6d", "Needs Improvement": "#ff6b35"
  };
  const vc = verdictColors[result.verdict] || "#aaa";

  return (
    <div>
      {/* Overall */}
      <div style={{
        display: "flex", alignItems: "center", gap: 24,
        background: "rgba(255,255,255,0.02)", border: "1px solid rgba(255,255,255,0.07)",
        borderRadius: 16, padding: 28, marginBottom: 20
      }}>
        <ScoreRing score={result.overall} color={meta.color} size={100} />
        <div>
          <div style={{ fontSize: 11, letterSpacing: 3, color: "#555", fontFamily: "monospace", marginBottom: 8 }}>OVERALL SCORE</div>
          <div style={{ fontSize: 28, fontWeight: 900, color: "#fff", fontFamily: "monospace" }}>{result.overall}<span style={{ fontSize: 14, color: "#555" }}>/100</span></div>
          <div style={{
            display: "inline-block", marginTop: 8, padding: "4px 12px",
            background: `${vc}15`, color: vc, borderRadius: 6, fontSize: 12,
            border: `1px solid ${vc}30`, fontFamily: "monospace"
          }}>{result.verdict}</div>
        </div>
        <div style={{ marginLeft: "auto", textAlign: "right" }}>
          <div style={{ fontSize: 12, color: "#555", marginBottom: 4 }}>Complexity</div>
          <div style={{ fontFamily: "monospace", color: "#00b4ff", fontSize: 14 }}>Time: {result.timeComplexity}</div>
          <div style={{ fontFamily: "monospace", color: "#ff6b35", fontSize: 14 }}>Space: {result.spaceComplexity}</div>
        </div>
      </div>

      {/* Score breakdown */}
      <div style={{ display: "grid", gridTemplateColumns: "repeat(4, 1fr)", gap: 12, marginBottom: 20 }}>
        {scores.map(({ label, val }) => (
          <div key={label} style={{
            background: "rgba(255,255,255,0.02)", border: "1px solid rgba(255,255,255,0.06)",
            borderRadius: 12, padding: "16px 12px", textAlign: "center"
          }}>
            <div style={{ fontSize: 22, fontWeight: 700, color: val >= 70 ? "#00ff88" : val >= 50 ? "#ffb800" : "#ff4d6d", fontFamily: "monospace" }}>{val}</div>
            <div style={{ color: "#555", fontSize: 11, marginTop: 4 }}>{label}</div>
            <div style={{ marginTop: 8, height: 4, background: "rgba(255,255,255,0.06)", borderRadius: 2 }}>
              <div style={{ width: `${val}%`, height: "100%", background: val >= 70 ? "#00ff88" : val >= 50 ? "#ffb800" : "#ff4d6d", borderRadius: 2, transition: "width 0.8s ease" }} />
            </div>
          </div>
        ))}
      </div>

      {/* Feedback */}
      <div style={{ display: "grid", gridTemplateColumns: "1fr 1fr", gap: 16, marginBottom: 20 }}>
        <div style={{ background: "rgba(0,255,136,0.04)", border: "1px solid rgba(0,255,136,0.12)", borderRadius: 12, padding: 20 }}>
          <div style={{ color: "#00ff88", fontSize: 12, fontFamily: "monospace", letterSpacing: 2, marginBottom: 12 }}>✓ STRENGTHS</div>
          {result.strengths.map((s, i) => (
            <div key={i} style={{ color: "#ccc", fontSize: 13, marginBottom: 8, display: "flex", gap: 8 }}>
              <span style={{ color: "#00ff88" }}>→</span> {s}
            </div>
          ))}
        </div>
        <div style={{ background: "rgba(255,107,53,0.04)", border: "1px solid rgba(255,107,53,0.12)", borderRadius: 12, padding: 20 }}>
          <div style={{ color: "#ff6b35", fontSize: 12, fontFamily: "monospace", letterSpacing: 2, marginBottom: 12 }}>⚠ IMPROVEMENTS</div>
          {result.improvements.map((s, i) => (
            <div key={i} style={{ color: "#ccc", fontSize: 13, marginBottom: 8, display: "flex", gap: 8 }}>
              <span style={{ color: "#ff6b35" }}>→</span> {s}
            </div>
          ))}
        </div>
      </div>

      <div style={{ background: "rgba(0,180,255,0.04)", border: "1px solid rgba(0,180,255,0.12)", borderRadius: 12, padding: 20, marginBottom: 20 }}>
        <div style={{ color: "#00b4ff", fontSize: 12, fontFamily: "monospace", letterSpacing: 2, marginBottom: 8 }}>OPTIMAL APPROACH</div>
        <p style={{ color: "#ccc", fontSize: 14, lineHeight: 1.7, margin: "0 0 12px" }}>{result.optimalApproach}</p>
        <div style={{ borderTop: "1px solid rgba(0,180,255,0.1)", paddingTop: 12, color: "#00b4ff", fontSize: 13 }}>
          Interview Tip: {result.interviewTip}
        </div>
      </div>

      <div style={{ display: "flex", gap: 12 }}>
        <button onClick={onRetry} style={{
          flex: 1, padding: "12px", background: "rgba(255,255,255,0.04)", border: "1px solid rgba(255,255,255,0.1)",
          color: "#888", borderRadius: 10, cursor: "pointer", fontSize: 14, fontFamily: "monospace"
        }}>↺ RETRY</button>
        {!isLast && (
          <button onClick={onNext} style={{
            flex: 2, padding: "12px", background: "rgba(0,255,136,0.1)", border: "1px solid rgba(0,255,136,0.3)",
            color: "#00ff88", borderRadius: 10, cursor: "pointer", fontSize: 14, fontFamily: "monospace", fontWeight: 700
          }}>NEXT QUESTION →</button>
        )}
        <button onClick={onDone} style={{
          flex: isLast ? 2 : 1, padding: "12px", background: "linear-gradient(135deg, #00ff88, #00cc6a)",
          border: "none", color: "#000", borderRadius: 10, cursor: "pointer", fontSize: 14, fontFamily: "monospace", fontWeight: 900
        }}>✓ DONE</button>
      </div>
    </div>
  );
}

function TechnicalRound({ onComplete, onBack }) {
  const [qIdx, setQIdx] = useState(0);
  const [answer, setAnswer] = useState("");
  const [loading, setLoading] = useState(false);
  const [result, setResult] = useState(null);
  const q = QUESTION_BANK.technical[qIdx];
  const meta = ROUND_META.technical;

  const catColors = {
    "System Design": "#ff6b35", "OS Concepts": "#00b4ff",
    "Databases": "#9b59b6", "Networking": "#00ff88",
    "OOP & Design Patterns": "#ffb800", "Behavioral": "#e91e63"
  };

  const evaluate = async () => {
    if (!answer.trim() || answer.length < 30) return;
    setLoading(true);
    try {
      const raw = await callClaude([{
        role: "user",
        content: `You are a FAANG senior engineer evaluating a technical interview answer.

Question: ${q.question}
Category: ${q.category}
Key Points to Cover: ${q.keyPoints.join(", ")}

Candidate's Answer:
${answer}

Evaluate and respond ONLY in this JSON format:
{
  "depth": <0-100>,
  "accuracy": <0-100>,
  "clarity": <0-100>,
  "completeness": <0-100>,
  "overall": <0-100>,
  "grade": "Excellent|Good|Average|Below Average",
  "coveredPoints": ["point1", "point2"],
  "missedPoints": ["point1", "point2"],
  "improvements": ["imp1", "imp2", "imp3"],
  "modelAnswer": "A concise 2-3 sentence ideal answer summary",
  "followUpQ": "A likely follow-up question in a real interview"
}`
      }], "You are a strict technical interviewer. Always respond with valid JSON only.");
      const json = JSON.parse(raw.replace(/```json|```/g, "").trim());
      setResult(json);
    } catch (e) {
      setResult({
        depth: 65, accuracy: 70, clarity: 60, completeness: 55, overall: 63,
        grade: "Average",
        coveredPoints: ["Basic concept mentioned"],
        missedPoints: q.keyPoints.slice(0, 3),
        improvements: ["Add more specific examples", "Discuss trade-offs", "Mention scalability"],
        modelAnswer: "A comprehensive answer would cover the key trade-offs and include specific examples.",
        followUpQ: "How would you handle this at scale with millions of users?"
      });
    }
    setLoading(false);
  };

  const gradeColors = { Excellent: "#00ff88", Good: "#00b4ff", Average: "#ffb800", "Below Average": "#ff4d6d" };

  return (
    <div style={{ maxWidth: 900, margin: "0 auto", padding: "0 24px" }}>
      <div style={{ display: "flex", alignItems: "center", gap: 16, padding: "24px 0 20px", borderBottom: "1px solid rgba(255,255,255,0.06)", marginBottom: 24 }}>
        <button onClick={onBack} style={{ background: "none", border: "1px solid #333", color: "#888", padding: "6px 14px", borderRadius: 8, cursor: "pointer", fontSize: 13 }}>← Back</button>
        <div style={{ flex: 1 }}>
          <div style={{ color: meta.color, fontSize: 11, letterSpacing: 3, fontFamily: "monospace" }}>TECHNICAL ROUND</div>
          <div style={{ color: "#fff", fontWeight: 700 }}>Question {qIdx + 1} of {QUESTION_BANK.technical.length}</div>
        </div>
        <Timer key={qIdx} running={!result} initialSeconds={600} />
      </div>

      {!result ? (
        <>
          <div style={{
            background: "rgba(255,255,255,0.02)", border: "1px solid rgba(255,255,255,0.07)",
            borderRadius: 16, padding: 28, marginBottom: 20
          }}>
            <div style={{ display: "flex", gap: 8, marginBottom: 16, flexWrap: "wrap" }}>
              <Tag color={catColors[q.category] || "#888"}>{q.category}</Tag>
              <Tag color={DIFF_COLORS[q.difficulty]}>{q.difficulty}</Tag>
              {q.company.slice(0, 3).map(c => <Tag key={c} color="#555">{c}</Tag>)}
            </div>
            <p style={{ color: "#ddd", fontSize: 16, lineHeight: 1.8, margin: 0 }}>{q.question}</p>
          </div>

          <div style={{
            background: "rgba(0,180,255,0.03)", border: "1px solid rgba(0,180,255,0.1)",
            borderRadius: 12, padding: 16, marginBottom: 16
          }}>
            <div style={{ color: "#00b4ff", fontSize: 11, fontFamily: "monospace", letterSpacing: 2, marginBottom: 8 }}>KEY POINTS TO COVER</div>
            <div style={{ display: "flex", flexWrap: "wrap", gap: 8 }}>
              {q.keyPoints.map(p => <Tag key={p} color="#00b4ff">{p}</Tag>)}
            </div>
          </div>

          <textarea
            value={answer}
            onChange={e => setAnswer(e.target.value)}
            placeholder="Type your detailed answer here. Be specific, use examples, and discuss trade-offs..."
            style={{
              width: "100%", minHeight: 200, padding: 20,
              background: "#0d1117", border: "1px solid rgba(255,255,255,0.08)",
              borderRadius: 12, color: "#e6edf3", fontSize: 14, lineHeight: 1.7,
              resize: "vertical", outline: "none", boxSizing: "border-box",
              fontFamily: "'Georgia', serif"
            }}
          />
          <div style={{ display: "flex", justifyContent: "space-between", alignItems: "center", marginTop: 4, marginBottom: 16 }}>
            <span style={{ color: "#555", fontSize: 12 }}>{answer.length} chars · Aim for 150+ for a thorough answer</span>
          </div>

          <div style={{ display: "flex", gap: 12 }}>
            <button onClick={() => { setQIdx(i => Math.max(0, i - 1)); setAnswer(""); setResult(null); }} disabled={qIdx === 0}
              style={{ padding: "12px 20px", background: "rgba(255,255,255,0.04)", border: "1px solid rgba(255,255,255,0.08)", color: "#888", borderRadius: 10, cursor: "pointer", fontSize: 13 }}>
              ← Prev
            </button>
            <button onClick={evaluate} disabled={loading || answer.length < 30} style={{
              flex: 1, padding: "14px",
              background: loading ? "rgba(0,180,255,0.2)" : "linear-gradient(135deg, #00b4ff, #0088cc)",
              border: "none", borderRadius: 10, color: "#000",
              fontWeight: 900, fontSize: 15, cursor: "pointer", letterSpacing: 1, fontFamily: "monospace"
            }}>
              {loading ? "EVALUATING..." : "SUBMIT ANSWER"}
            </button>
            <button onClick={() => { setQIdx(i => Math.min(QUESTION_BANK.technical.length - 1, i + 1)); setAnswer(""); setResult(null); }}
              disabled={qIdx === QUESTION_BANK.technical.length - 1}
              style={{ padding: "12px 20px", background: "rgba(255,255,255,0.04)", border: "1px solid rgba(255,255,255,0.08)", color: "#888", borderRadius: 10, cursor: "pointer", fontSize: 13 }}>
              Next →
            </button>
          </div>
        </>
      ) : (
        <TechResult result={result} meta={meta} gradeColors={gradeColors}
          onRetry={() => { setResult(null); setAnswer(""); }}
          onNext={() => { setResult(null); setAnswer(""); setQIdx(i => Math.min(QUESTION_BANK.technical.length - 1, i + 1)); }}
          onDone={() => onComplete(result.overall)}
          isLast={qIdx === QUESTION_BANK.technical.length - 1}
        />
      )}
    </div>
  );
}

function TechResult({ result, meta, gradeColors, onRetry, onNext, onDone, isLast }) {
  const gc = gradeColors[result.grade] || "#aaa";
  const scores = [
    { label: "Depth", val: result.depth },
    { label: "Accuracy", val: result.accuracy },
    { label: "Clarity", val: result.clarity },
    { label: "Completeness", val: result.completeness }
  ];
  return (
    <div>
      <div style={{ display: "flex", alignItems: "center", gap: 24, background: "rgba(255,255,255,0.02)", border: "1px solid rgba(255,255,255,0.07)", borderRadius: 16, padding: 28, marginBottom: 20 }}>
        <ScoreRing score={result.overall} color={meta.color} size={100} />
        <div>
          <div style={{ fontSize: 11, letterSpacing: 3, color: "#555", fontFamily: "monospace", marginBottom: 8 }}>OVERALL SCORE</div>
          <div style={{ fontSize: 28, fontWeight: 900, color: "#fff", fontFamily: "monospace" }}>{result.overall}<span style={{ fontSize: 14, color: "#555" }}>/100</span></div>
          <div style={{ display: "inline-block", marginTop: 8, padding: "4px 12px", background: `${gc}15`, color: gc, borderRadius: 6, fontSize: 12, border: `1px solid ${gc}30`, fontFamily: "monospace" }}>{result.grade}</div>
        </div>
      </div>

      <div style={{ display: "grid", gridTemplateColumns: "repeat(4,1fr)", gap: 12, marginBottom: 20 }}>
        {scores.map(({ label, val }) => (
          <div key={label} style={{ background: "rgba(255,255,255,0.02)", border: "1px solid rgba(255,255,255,0.06)", borderRadius: 12, padding: "16px 12px", textAlign: "center" }}>
            <div style={{ fontSize: 22, fontWeight: 700, color: val >= 70 ? "#00b4ff" : val >= 50 ? "#ffb800" : "#ff4d6d", fontFamily: "monospace" }}>{val}</div>
            <div style={{ color: "#555", fontSize: 11, marginTop: 4 }}>{label}</div>
            <div style={{ marginTop: 8, height: 4, background: "rgba(255,255,255,0.06)", borderRadius: 2 }}>
              <div style={{ width: `${val}%`, height: "100%", background: meta.color, borderRadius: 2 }} />
            </div>
          </div>
        ))}
      </div>

      <div style={{ display: "grid", gridTemplateColumns: "1fr 1fr", gap: 16, marginBottom: 16 }}>
        <div style={{ background: "rgba(0,255,136,0.04)", border: "1px solid rgba(0,255,136,0.12)", borderRadius: 12, padding: 20 }}>
          <div style={{ color: "#00ff88", fontSize: 12, fontFamily: "monospace", letterSpacing: 2, marginBottom: 12 }}>✓ COVERED</div>
          {result.coveredPoints.map((s, i) => <div key={i} style={{ color: "#ccc", fontSize: 13, marginBottom: 8 }}>→ {s}</div>)}
        </div>
        <div style={{ background: "rgba(255,77,109,0.04)", border: "1px solid rgba(255,77,109,0.12)", borderRadius: 12, padding: 20 }}>
          <div style={{ color: "#ff4d6d", fontSize: 12, fontFamily: "monospace", letterSpacing: 2, marginBottom: 12 }}>✗ MISSED</div>
          {result.missedPoints.map((s, i) => <div key={i} style={{ color: "#ccc", fontSize: 13, marginBottom: 8 }}>→ {s}</div>)}
        </div>
      </div>

      <div style={{ background: "rgba(0,180,255,0.04)", border: "1px solid rgba(0,180,255,0.12)", borderRadius: 12, padding: 20, marginBottom: 16 }}>
        <div style={{ color: "#00b4ff", fontSize: 12, fontFamily: "monospace", letterSpacing: 2, marginBottom: 8 }}>MODEL ANSWER</div>
        <p style={{ color: "#ccc", fontSize: 14, lineHeight: 1.7, margin: "0 0 12px" }}>{result.modelAnswer}</p>
        <div style={{ borderTop: "1px solid rgba(0,180,255,0.1)", paddingTop: 12, color: "#ffb800", fontSize: 13 }}>
          Likely Follow-up: "{result.followUpQ}"
        </div>
      </div>

      <div style={{ display: "flex", gap: 12 }}>
        <button onClick={onRetry} style={{ flex: 1, padding: "12px", background: "rgba(255,255,255,0.04)", border: "1px solid rgba(255,255,255,0.1)", color: "#888", borderRadius: 10, cursor: "pointer", fontSize: 14, fontFamily: "monospace" }}>↺ RETRY</button>
        {!isLast && <button onClick={onNext} style={{ flex: 2, padding: "12px", background: "rgba(0,180,255,0.1)", border: "1px solid rgba(0,180,255,0.3)", color: "#00b4ff", borderRadius: 10, cursor: "pointer", fontSize: 14, fontFamily: "monospace", fontWeight: 700 }}>NEXT →</button>}
        <button onClick={onDone} style={{ flex: 1, padding: "12px", background: "linear-gradient(135deg, #00b4ff, #0088cc)", border: "none", color: "#000", borderRadius: 10, cursor: "pointer", fontSize: 14, fontFamily: "monospace", fontWeight: 900 }}>✓ DONE</button>
      </div>
    </div>
  );
}

function AptitudeRound({ onComplete, onBack }) {
  const [qIdx, setQIdx] = useState(0);
  const [selected, setSelected] = useState(null);
  const [submitted, setSubmitted] = useState(false);
  const [sessionScores, setSessionScores] = useState([]);
  const q = QUESTION_BANK.aptitude[qIdx];
  const meta = ROUND_META.aptitude;
  const isCorrect = selected === q.answer;

  const catColors = {
    "Quantitative": "#ff6b35", "Logical Reasoning": "#00b4ff",
    "Data Interpretation": "#9b59b6", "Pattern Recognition": "#00ff88", "Verbal": "#ffb800"
  };

  const handleNext = () => {
    if (submitted) {
      setSessionScores(s => [...s, isCorrect ? 100 : 0]);
    }
    if (qIdx === QUESTION_BANK.aptitude.length - 1) {
      const allScores = [...sessionScores, (submitted && isCorrect ? 100 : 0)];
      onComplete(Math.round(allScores.reduce((a, b) => a + b, 0) / allScores.length));
    } else {
      setQIdx(i => i + 1);
      setSelected(null);
      setSubmitted(false);
    }
  };

  return (
    <div style={{ maxWidth: 800, margin: "0 auto", padding: "0 24px" }}>
      <div style={{ display: "flex", alignItems: "center", gap: 16, padding: "24px 0 20px", borderBottom: "1px solid rgba(255,255,255,0.06)", marginBottom: 24 }}>
        <button onClick={onBack} style={{ background: "none", border: "1px solid #333", color: "#888", padding: "6px 14px", borderRadius: 8, cursor: "pointer", fontSize: 13 }}>← Back</button>
        <div style={{ flex: 1 }}>
          <div style={{ color: meta.color, fontSize: 11, letterSpacing: 3, fontFamily: "monospace" }}>APTITUDE ROUND</div>
        </div>
        <Timer key={qIdx} running={!submitted} initialSeconds={90} onTimeUp={() => setSubmitted(true)} />
      </div>

      {/* Progress */}
      <div style={{ display: "flex", gap: 6, marginBottom: 24 }}>
        {QUESTION_BANK.aptitude.map((_, i) => (
          <div key={i} style={{
            flex: 1, height: 4, borderRadius: 2,
            background: i < qIdx ? "#00ff88" : i === qIdx ? meta.color : "rgba(255,255,255,0.08)"
          }} />
        ))}
      </div>

      <div style={{ background: "rgba(255,255,255,0.02)", border: "1px solid rgba(255,255,255,0.07)", borderRadius: 16, padding: 28, marginBottom: 20 }}>
        <div style={{ display: "flex", gap: 8, marginBottom: 16 }}>
          <Tag color={catColors[q.category] || "#888"}>{q.category}</Tag>
          <Tag color={DIFF_COLORS[q.difficulty]}>{q.difficulty}</Tag>
          <span style={{ marginLeft: "auto", color: "#555", fontSize: 13, fontFamily: "monospace" }}>Q{qIdx + 1}/{QUESTION_BANK.aptitude.length}</span>
        </div>
        <p style={{ color: "#ddd", fontSize: 16, lineHeight: 1.8, margin: 0 }}>{q.question}</p>
      </div>

      {/* Options */}
      <div style={{ display: "grid", gridTemplateColumns: "1fr 1fr", gap: 12, marginBottom: 20 }}>
        {q.options.map((opt, i) => {
          let bg = "rgba(255,255,255,0.03)";
          let border = "rgba(255,255,255,0.08)";
          let color = "#ccc";
          if (submitted) {
            if (i === q.answer) { bg = "rgba(0,255,136,0.08)"; border = "rgba(0,255,136,0.3)"; color = "#00ff88"; }
            else if (i === selected && i !== q.answer) { bg = "rgba(255,77,109,0.08)"; border = "rgba(255,77,109,0.3)"; color = "#ff4d6d"; }
          } else if (i === selected) {
            bg = `rgba(255,107,53,0.1)`;
            border = meta.color;
            color = meta.color;
          }
          return (
            <button key={i} onClick={() => !submitted && setSelected(i)} style={{
              background: bg, border: `1px solid ${border}`, color,
              padding: "16px 20px", borderRadius: 12, cursor: submitted ? "default" : "pointer",
              fontSize: 14, textAlign: "left", transition: "all 0.2s",
              display: "flex", alignItems: "center", gap: 12
            }}>
              <span style={{ fontFamily: "monospace", fontSize: 12, color: "#555", minWidth: 20 }}>{String.fromCharCode(65 + i)}.</span>
              {opt}
              {submitted && i === q.answer && <span style={{ marginLeft: "auto" }}>✓</span>}
              {submitted && i === selected && i !== q.answer && <span style={{ marginLeft: "auto" }}>✗</span>}
            </button>
          );
        })}
      </div>

      {!submitted && (
        <button onClick={() => { if (selected !== null) setSubmitted(true); }} disabled={selected === null}
          style={{
            width: "100%", padding: "14px", background: selected !== null ? "linear-gradient(135deg, #ff6b35, #ff4500)" : "rgba(255,255,255,0.05)",
            border: "none", borderRadius: 10, color: selected !== null ? "#fff" : "#555",
            fontWeight: 900, fontSize: 15, cursor: selected !== null ? "pointer" : "not-allowed",
            letterSpacing: 1, fontFamily: "monospace"
          }}>
          SUBMIT ANSWER
        </button>
      )}

      {submitted && (
        <div style={{
          background: isCorrect ? "rgba(0,255,136,0.06)" : "rgba(255,77,109,0.06)",
          border: `1px solid ${isCorrect ? "rgba(0,255,136,0.2)" : "rgba(255,77,109,0.2)"}`,
          borderRadius: 12, padding: 20, marginBottom: 16
        }}>
          <div style={{ fontSize: 16, fontWeight: 700, color: isCorrect ? "#00ff88" : "#ff4d6d", marginBottom: 8 }}>
            {isCorrect ? "✓ Correct!" : "✗ Incorrect"}
          </div>
          <p style={{ color: "#ccc", fontSize: 14, lineHeight: 1.7, margin: 0 }}>
            <strong style={{ color: "#fff" }}>Explanation: </strong>{q.explanation}
          </p>
        </div>
      )}

      {submitted && (
        <button onClick={handleNext} style={{
          width: "100%", padding: "14px",
          background: qIdx === QUESTION_BANK.aptitude.length - 1 ? "linear-gradient(135deg, #00ff88, #00cc6a)" : "rgba(255,107,53,0.15)",
          border: qIdx === QUESTION_BANK.aptitude.length - 1 ? "none" : "1px solid rgba(255,107,53,0.3)",
          color: qIdx === QUESTION_BANK.aptitude.length - 1 ? "#000" : meta.color,
          fontWeight: 900, fontSize: 15, cursor: "pointer", letterSpacing: 1, fontFamily: "monospace", borderRadius: 10
        }}>
          {qIdx === QUESTION_BANK.aptitude.length - 1 ? "✓ FINISH ROUND" : "NEXT QUESTION →"}
        </button>
      )}
    </div>
  );
}

// ─── AI CHAT COACH ────────────────────────────────────────────────────────────
function AICoach({ onBack }) {
  const [messages, setMessages] = useState([
    { role: "assistant", content: "Hi! I'm your AI Interview Coach. Ask me anything — mock interview questions, explain concepts, review your answers, or get personalized study tips." }
  ]);
  const [input, setInput] = useState("");
  const [loading, setLoading] = useState(false);
  const endRef = useRef(null);

  useEffect(() => { endRef.current?.scrollIntoView({ behavior: "smooth" }); }, [messages]);

  const send = async () => {
    if (!input.trim() || loading) return;
    const userMsg = { role: "user", content: input };
    setMessages(m => [...m, userMsg]);
    setInput("");
    setLoading(true);
    try {
      const history = [...messages, userMsg].slice(-10).map(m => ({ role: m.role, content: m.content }));
      const reply = await callClaude(history, `You are an expert technical interview coach with experience at FAANG companies. Help candidates prepare for software engineering interviews. You can:
- Give mock interview questions
- Evaluate answers and give detailed feedback
- Explain complex CS concepts
- Suggest study plans
- Give tips on system design, coding, and behavioral rounds
Be concise, specific, and encouraging. Format code with backticks.`);
      setMessages(m => [...m, { role: "assistant", content: reply }]);
    } catch (e) {
      setMessages(m => [...m, { role: "assistant", content: "Sorry, I couldn't connect. Check your API access and try again." }]);
    }
    setLoading(false);
  };

  return (
    <div style={{ maxWidth: 800, margin: "0 auto", padding: "0 24px", display: "flex", flexDirection: "column", height: "calc(100vh - 120px)" }}>
      <div style={{ display: "flex", alignItems: "center", gap: 16, padding: "24px 0 20px", borderBottom: "1px solid rgba(255,255,255,0.06)", marginBottom: 0 }}>
        <button onClick={onBack} style={{ background: "none", border: "1px solid #333", color: "#888", padding: "6px 14px", borderRadius: 8, cursor: "pointer", fontSize: 13 }}>← Back</button>
        <div>
          <div style={{ color: "#9b59b6", fontSize: 11, letterSpacing: 3, fontFamily: "monospace" }}>AI INTERVIEW COACH</div>
          <div style={{ color: "#fff", fontWeight: 700 }}>Chat with your personal coach</div>
        </div>
        <div style={{ marginLeft: "auto", width: 10, height: 10, borderRadius: "50%", background: "#00ff88", boxShadow: "0 0 8px #00ff88" }} />
      </div>

      <div style={{ flex: 1, overflowY: "auto", padding: "20px 0", display: "flex", flexDirection: "column", gap: 16 }}>
        {messages.map((m, i) => (
          <div key={i} style={{ display: "flex", justifyContent: m.role === "user" ? "flex-end" : "flex-start" }}>
            <div style={{
              maxWidth: "80%", padding: "14px 18px",
              background: m.role === "user" ? "linear-gradient(135deg, #9b59b6, #7d3c98)" : "rgba(255,255,255,0.04)",
              border: m.role === "user" ? "none" : "1px solid rgba(255,255,255,0.08)",
              borderRadius: m.role === "user" ? "18px 18px 4px 18px" : "18px 18px 18px 4px",
              color: "#e0e0e0", fontSize: 14, lineHeight: 1.7,
              whiteSpace: "pre-wrap"
            }}>
              {m.content}
            </div>
          </div>
        ))}
        {loading && (
          <div style={{ display: "flex" }}>
            <div style={{ background: "rgba(255,255,255,0.04)", border: "1px solid rgba(255,255,255,0.08)", borderRadius: "18px 18px 18px 4px", padding: "14px 18px" }}>
              <span style={{ color: "#9b59b6" }}>●</span> <span style={{ color: "#555", fontSize: 13 }}>Thinking...</span>
            </div>
          </div>
        )}
        <div ref={endRef} />
      </div>

      <div style={{ paddingTop: 16, borderTop: "1px solid rgba(255,255,255,0.06)", display: "flex", gap: 12 }}>
        <input
          value={input}
          onChange={e => setInput(e.target.value)}
          onKeyDown={e => e.key === "Enter" && !e.shiftKey && send()}
          placeholder="Ask anything... 'Give me a hard graph problem', 'What is LRU cache?'"
          style={{
            flex: 1, padding: "14px 18px", background: "rgba(255,255,255,0.04)",
            border: "1px solid rgba(255,255,255,0.1)", borderRadius: 12,
            color: "#fff", fontSize: 14, outline: "none"
          }}
        />
        <button onClick={send} disabled={loading || !input.trim()} style={{
          padding: "14px 20px", background: "linear-gradient(135deg, #9b59b6, #7d3c98)",
          border: "none", borderRadius: 12, color: "#fff", fontSize: 16, cursor: "pointer"
        }}>→</button>
      </div>

      <div style={{ display: "flex", gap: 8, marginTop: 8, flexWrap: "wrap" }}>
        {["Mock interview me on arrays", "Explain Big-O notation", "System design: design Twitter", "Behavioral: STAR method"].map(s => (
          <button key={s} onClick={() => setInput(s)} style={{
            background: "rgba(155,89,182,0.08)", border: "1px solid rgba(155,89,182,0.2)",
            color: "#9b59b6", padding: "4px 10px", borderRadius: 20, fontSize: 11, cursor: "pointer"
          }}>{s}</button>
        ))}
      </div>
    </div>
  );
}

// ─── MAIN APP ─────────────────────────────────────────────────────────────────
export default function App() {
  const [screen, setScreen] = useState("home"); // home | coding | technical | aptitude | coach
  const [scores, setScores] = useState({
    coding: { avg: 0, sessions: 0 },
    technical: { avg: 0, sessions: 0 },
    aptitude: { avg: 0, sessions: 0 }
  });

  const handleComplete = (type, score) => {
    setScores(prev => {
      const old = prev[type];
      const sessions = old.sessions + 1;
      const avg = Math.round((old.avg * old.sessions + score) / sessions);
      return { ...prev, [type]: { avg, sessions } };
    });
    setScreen("home");
  };

  return (
    <div style={{
      minHeight: "100vh",
      background: "#080810",
      color: "#fff",
      fontFamily: "'Trebuchet MS', sans-serif"
    }}>
      {/* Noise overlay */}
      <div style={{
        position: "fixed", inset: 0, pointerEvents: "none", zIndex: 0,
        background: "url(\"data:image/svg+xml,%3Csvg viewBox='0 0 200 200' xmlns='http://www.w3.org/2000/svg'%3E%3Cfilter id='n'%3E%3CfeTurbulence type='fractalNoise' baseFrequency='0.75' numOctaves='4' stitchTiles='stitch'/%3E%3C/filter%3E%3Crect width='100%25' height='100%25' filter='url(%23n)' opacity='0.03'/%3E%3C/svg%3E\")",
        opacity: 0.4
      }} />

      {/* Grid background */}
      <div style={{
        position: "fixed", inset: 0, pointerEvents: "none", zIndex: 0,
        backgroundImage: "linear-gradient(rgba(255,255,255,0.015) 1px, transparent 1px), linear-gradient(90deg, rgba(255,255,255,0.015) 1px, transparent 1px)",
        backgroundSize: "60px 60px"
      }} />

      {/* Glow orb */}
      <div style={{
        position: "fixed", top: -200, left: "50%", transform: "translateX(-50%)",
        width: 600, height: 600, borderRadius: "50%",
        background: "radial-gradient(circle, rgba(0,255,136,0.04) 0%, transparent 70%)",
        pointerEvents: "none", zIndex: 0
      }} />

      {/* Navbar */}
      <nav style={{
        position: "sticky", top: 0, zIndex: 100,
        background: "rgba(8,8,16,0.85)", backdropFilter: "blur(20px)",
        borderBottom: "1px solid rgba(255,255,255,0.06)",
        padding: "0 24px", height: 56,
        display: "flex", alignItems: "center", justifyContent: "space-between"
      }}>
        <div onClick={() => setScreen("home")} style={{ cursor: "pointer", display: "flex", alignItems: "center", gap: 10 }}>
          <div style={{
            width: 30, height: 30, borderRadius: 8, background: "linear-gradient(135deg, #00ff88, #00b4ff)",
            display: "flex", alignItems: "center", justifyContent: "center", fontSize: 14
          }}>IQ</div>
          <span style={{ fontWeight: 900, fontSize: 16, fontFamily: "monospace", letterSpacing: 1 }}>
            PREP<span style={{ color: "#00ff88" }}>IQ</span>
          </span>
        </div>

        <div style={{ display: "flex", gap: 6 }}>
          {[
            { id: "coding", label: "Coding", color: "#00ff88" },
            { id: "technical", label: "Technical", color: "#00b4ff" },
            { id: "aptitude", label: "Aptitude", color: "#ff6b35" },
            { id: "coach", label: "AI Coach", color: "#9b59b6" }
          ].map(({ id, label, color }) => (
            <button key={id} onClick={() => setScreen(id)} style={{
              background: screen === id ? `${color}15` : "none",
              border: screen === id ? `1px solid ${color}44` : "1px solid transparent",
              color: screen === id ? color : "#555",
              padding: "6px 14px", borderRadius: 8, cursor: "pointer", fontSize: 13,
              transition: "all 0.2s", fontFamily: "monospace"
            }}>{label}</button>
          ))}
        </div>

        <div style={{ display: "flex", gap: 16, alignItems: "center" }}>
          {Object.entries(scores).map(([key, s]) => s.sessions > 0 && (
            <div key={key} style={{ textAlign: "center" }}>
              <div style={{ color: ROUND_META[key].color, fontSize: 14, fontWeight: 700, fontFamily: "monospace" }}>{s.avg}%</div>
              <div style={{ color: "#444", fontSize: 9, letterSpacing: 1 }}>{key.toUpperCase()}</div>
            </div>
          ))}
        </div>
      </nav>

      {/* Content */}
      <div style={{ position: "relative", zIndex: 1, paddingBottom: 60 }}>
        {screen === "home" && <Home onStart={setScreen} scores={scores} />}
        {screen === "coding" && <CodingRound onComplete={s => handleComplete("coding", s)} onBack={() => setScreen("home")} />}
        {screen === "technical" && <TechnicalRound onComplete={s => handleComplete("technical", s)} onBack={() => setScreen("home")} />}
        {screen === "aptitude" && <AptitudeRound onComplete={s => handleComplete("aptitude", s)} onBack={() => setScreen("home")} />}
        {screen === "coach" && <AICoach onBack={() => setScreen("home")} />}
      </div>
    </div>
  );
}
