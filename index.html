import React, { useState, useEffect, useRef } from "react";

// ReviewBuddy - Single-file React app
// Drop this file into a React project (e.g. created with Vite or Create React App)
// Requires Tailwind CSS for styling. It's a single-page app that persists to localStorage.

const SAMPLE_LESSONS = {
  Mathematics: [
    { id: 'angles', title: 'Angles', resources: [], exercises: [] },
    { id: 'basic-algebra', title: 'Basic Algebra', resources: [], exercises: [] },
    { id: 'basic-calculus', title: 'Basic Calculus', resources: [], exercises: [] },
    { id: 'business-math', title: 'Business Mathematics', resources: [], exercises: [] },
    { id: 'derivatives', title: 'Derivatives', resources: [], exercises: [] },
    { id: 'domain-range', title: 'Domain and Range', resources: [], exercises: [] },
    { id: 'euclidean', title: 'Euclidean & Non-Euclidean Geometry', resources: [], exercises: [] },
    { id: 'general-math', title: 'General Mathematics', resources: [], exercises: [] },
    { id: 'geometry', title: 'Geometry', resources: [], exercises: [] },
    { id: 'inequalities', title: 'Inequalities', resources: [], exercises: [] },
    { id: 'limitations', title: 'Limitations (Limits)', resources: [], exercises: [] },
    { id: 'linear-functions', title: 'Linear Functions', resources: [], exercises: [] },
    { id: 'logarithms', title: 'Logarithms', resources: [], exercises: [] },
    { id: 'mean-median-mode', title: 'Mean, Median & Mode', resources: [], exercises: [] },
    { id: 'permutations-prob', title: 'Permutations & Probability', resources: [], exercises: [] },
    { id: 'polynomial-factoring', title: 'Polynomial Factoring', resources: [], exercises: [] },
    { id: 'quadratic', title: 'Quadratic Equations', resources: [], exercises: [] },
    { id: 'rational-expr', title: 'Rational Expressions', resources: [], exercises: [] },
    { id: 'series-sequences', title: 'Series & Sequences', resources: [], exercises: [] },
    { id: 'interest', title: 'Simple & Compound Interest', resources: [], exercises: [] },
    { id: 'slope-graph', title: 'Slope & Graph', resources: [], exercises: [] },
    { id: 'std-dev', title: 'Standard Deviation', resources: [], exercises: [] },
    { id: 'statistics', title: 'Statistics', resources: [], exercises: [] },
    { id: 'triangle-postulates', title: 'Triangle Postulates', resources: [], exercises: [] },
    { id: 'trigonometry', title: 'Trigonometry', resources: [], exercises: [] },
    { id: 'variance', title: 'Variance', resources: [], exercises: [] },
    { id: 'word-problems', title: 'Word Problems', resources: [], exercises: [] },
  ],
  "Language Proficiency": [
    { id: 'sentence-error', title: 'Sentence Error', resources: [], exercises: [] },
    { id: 'analogies', title: 'Analogies', resources: [], exercises: [] },
    { id: 'syn-ant', title: 'Synonyms & Antonyms', resources: [], exercises: [] },
    { id: 'comm-process', title: 'Communication Processes & Models', resources: [], exercises: [] },
    { id: 'concepts-play', title: 'Concepts of Play', resources: [], exercises: [] },
    { id: 'academic-papers', title: 'Academic & Professional Papers', resources: [], exercises: [] },
    { id: 'fallacies', title: 'Fallacies', resources: [], exercises: [] },
    { id: 'figures-speech', title: 'Figures of Speech', resources: [], exercises: [] },
    { id: 'identifying-errors', title: 'Identifying Errors', resources: [], exercises: [] },
    { id: 'lit-crit', title: 'Literary Criticism', resources: [], exercises: [] },
    { id: 'oral-comm', title: 'Oral Communication', resources: [], exercises: [] },
    { id: 'reading-comp', title: 'Reading Comprehension', resources: [], exercises: [] },
    { id: 'research-questions', title: 'Research-related Questions', resources: [], exercises: [] },
    { id: 'panlapi-usage', title: 'Panlapi & Rin/Din, Ng/Nang usage', resources: [], exercises: [] },
  ],
  Science: [
    { id: 'biology', title: 'Biology', resources: [], exercises: [] },
    { id: 'chemistry', title: 'Chemistry', resources: [], exercises: [] },
    { id: 'earth-life', title: 'Earth & Life Science', resources: [], exercises: [] },
    { id: 'physics', title: 'Physics', resources: [], exercises: [] },
  ],
  "Abstract Reasoning": [
    { id: 'patterns', title: 'Finding Patterns', resources: [], exercises: [] },
    { id: 'logical', title: 'Logical Reasoning', resources: [], exercises: [] },
    { id: 'verbal-abstract', title: 'Verbal & Abstract Reasoning', resources: [], exercises: [] },
    { id: 'syllogisms', title: 'Syllogisms', resources: [], exercises: [] },
  ],
  "General Information": [
    { id: 'inventors', title: 'Inventors', resources: [], exercises: [] },
    { id: 'ph-history', title: 'Philippine History', resources: [], exercises: [] },
    { id: 'world-religion', title: 'World Religion', resources: [], exercises: [] },
    { id: 'philosophers', title: 'Philosophers', resources: [], exercises: [] },
  ],
};

const STORAGE_KEY = 'reviewbuddy:data:v1';

function useLocalStorageState(key, initial) {
  const [state, setState] = useState(() => {
    try {
      const raw = localStorage.getItem(key);
      return raw ? JSON.parse(raw) : initial;
    } catch (e) {
      return initial;
    }
  });
  useEffect(() => {
    try { localStorage.setItem(key, JSON.stringify(state)); } catch (e) {}
  }, [key, state]);
  return [state, setState];
}

function App() {
  const [data, setData] = useLocalStorageState(STORAGE_KEY, {
    lessons: SAMPLE_LESSONS,
    quizzes: [],
    progress: {},
  });

  const [view, setView] = useState({ name: 'dashboard' });

  const openLesson = (category, lessonId) => setView({ name: 'lesson', category, lessonId });
  const openQuiz = (quizId) => setView({ name: 'quiz', quizId });

  const addResourceToLesson = (category, lessonId, resource) => {
    setData(prev => {
      const lessons = { ...prev.lessons };
      lessons[category] = lessons[category].map(l => l.id === lessonId ? { ...l, resources: [...l.resources, resource] } : l);
      return { ...prev, lessons };
    });
  };

  const addQuiz = (quiz) => {
    setData(prev => ({ ...prev, quizzes: [...prev.quizzes, { ...quiz, id: 'quiz_' + Date.now() }] }));
  };

  const saveQuizResult = (quizId, result) => {
    setData(prev => ({ ...prev, progress: { ...prev.progress, [quizId]: result } }));
  };

  const exportData = () => {
    const blob = new Blob([JSON.stringify(data, null, 2)], { type: 'application/json' });
    const url = URL.createObjectURL(blob);
    const a = document.createElement('a');
    a.href = url; a.download = 'reviewbuddy_export.json'; a.click();
    URL.revokeObjectURL(url);
  };

  const importData = (json) => {
    try {
      const parsed = typeof json === 'string' ? JSON.parse(json) : json;
      setData(parsed);
      alert('Imported data — please confirm lessons and quizzes.');
    } catch (e) { alert('Invalid JSON'); }
  };

  return (
    <div className="min-h-screen bg-slate-50 text-slate-800 p-4">
      <div className="max-w-6xl mx-auto">
        <Header setView={setView} exportData={exportData} importData={importData} />

        {view.name === 'dashboard' && (
          <Dashboard data={data} openLesson={openLesson} openQuiz={openQuiz} setView={setView} />
        )}

        {view.name === 'lesson' && (
          <LessonPage
            category={view.category}
            lessonId={view.lessonId}
            lessons={data.lessons}
            addResource={addResourceToLesson}
            goBack={() => setView({ name: 'dashboard' })}
          />
        )}

        {view.name === 'create-quiz' && (
          <QuizEditor
            lessons={data.lessons}
            onSave={(q) => { addQuiz(q); setView({ name: 'dashboard' }); }}
            onCancel={() => setView({ name: 'dashboard' })}
          />
        )}

        {view.name === 'quiz' && (
          <QuizRunner
            quiz={data.quizzes.find(q => q.id === view.quizId)}
            onSave={(res) => { saveQuizResult(view.quizId, res); setView({ name: 'dashboard' }); }}
            onCancel={() => setView({ name: 'dashboard' })}
          />
        )}

        <Footer />
      </div>
    </div>
  );
}

function Header({ setView, exportData, importData }) {
  const fileRef = useRef();
  return (
    <header className="flex items-center justify-between py-4">
      <h1 className="text-2xl font-bold">ReviewBuddy — Long-term Review Site</h1>
      <div className="flex gap-2">
        <button className="px-3 py-1 rounded bg-indigo-600 text-white" onClick={() => setView({ name: 'create-quiz' })}>Create Quiz</button>
        <button className="px-3 py-1 rounded bg-emerald-600 text-white" onClick={exportData}>Export Data</button>
        <label className="px-3 py-1 rounded bg-yellow-500 text-black cursor-pointer">
          Import
          <input ref={fileRef} type="file" accept="application/json" className="hidden" onChange={(e) => {
            const f = e.target.files[0]; if (!f) return;
            const reader = new FileReader();
            reader.onload = () => importData(reader.result);
            reader.readAsText(f);
          }} />
        </label>
        <button className="px-3 py-1 rounded bg-slate-200" onClick={() => {
          const twoWeeks = generateTwoWeekPlan();
          const blob = new Blob([JSON.stringify(twoWeeks, null, 2)], { type: 'application/json' });
          const url = URL.createObjectURL(blob);
          const a = document.createElement('a'); a.href = url; a.download = '2week_plan.json'; a.click(); URL.revokeObjectURL(url);
        }}>Download 2-week Plan</button>
      </div>
    </header>
  );
}

function Footer() {
  return (
    <footer className="mt-8 text-sm text-slate-600">Built for long-term use • Data saved in your browser • Export/Import to move between devices.</footer>
  );
}

function Dashboard({ data, openLesson, openQuiz, setView }) {
  return (
    <div className="grid grid-cols-1 md:grid-cols-3 gap-6">
      <div className="md:col-span-2 bg-white p-4 rounded shadow">
        <h2 className="text-lg font-semibold">Subjects</h2>
        <div className="mt-3 grid gap-2">
          {Object.entries(data.lessons).map(([category, lessons]) => (
            <div key={category} className="p-3 border rounded">
              <h3 className="font-medium">{category} <span className="text-sm text-slate-500">({lessons.length})</span></h3>
              <div className="mt-2 grid grid-cols-2 md:grid-cols-3 gap-2">
                {lessons.map(l => (
                  <button key={l.id} className="text-left p-2 border rounded hover:bg-slate-50" onClick={() => openLesson(category, l.id)}>
                    <div className="font-semibold">{l.title}</div>
                    <div className="text-sm text-slate-500">Resources: {l.resources.length}</div>
                  </button>
                ))}
              </div>
            </div>
          ))}
        </div>
      </div>

      <div className="bg-white p-4 rounded shadow">
        <h2 className="text-lg font-semibold">Quick Actions</h2>
        <div className="mt-3 flex flex-col gap-2">
          <button className="p-2 rounded bg-indigo-50" onClick={() => setView({ name: 'create-quiz' })}>Create a timed quiz</button>
          <div className="p-2 border rounded">
            <h4 className="font-medium">Saved Quizzes</h4>
            <div className="mt-2 space-y-2">
              {data.quizzes.length === 0 && <div className="text-sm text-slate-500">No quizzes yet — create one!</div>}
              {data.quizzes.map(q => (
                <div key={q.id} className="flex items-center justify-between">
                  <div>
                    <div className="font-semibold">{q.title}</div>
                    <div className="text-sm text-slate-500">{q.questions.length} questions • {q.timeLimitSec ? Math.round(q.timeLimitSec/60) : 0} min</div>
                  </div>
                  <div className="flex gap-2">
                    <button className="px-2 py-1 bg-emerald-100 rounded" onClick={() => openQuiz(q.id)}>Take</button>
                  </div>
                </div>
              ))}
            </div>
          </div>

          <div className="p-2 border rounded">
            <h4 className="font-medium">Progress</h4>
            <div className="mt-2 text-sm text-slate-500">You have {Object.keys(data.progress).length} saved quiz results.</div>
          </div>

        </div>
      </div>
    </div>
  );
}

function LessonPage({ category, lessonId, lessons, addResource, goBack }) {
  const lesson = lessons[category].find(l => l.id === lessonId);
  const [resUrl, setResUrl] = useState('');
  const [resType, setResType] = useState('youtube');
  const [note, setNote] = useState('');

  if (!lesson) return (
    <div className="bg-white p-4 rounded shadow">Lesson not found. <button onClick={goBack} className="underline">Go back</button></div>
  );

  const handleAdd = () => {
    if (!resUrl) return alert('Enter a URL or resource title');
    addResource(category, lessonId, { id: 'r_' + Date.now(), type: resType, url: resUrl, note });
    setResUrl(''); setNote('');
  };

  return (
    <div className="bg-white p-4 rounded shadow">
      <div className="flex items-center justify-between">
        <div>
          <h2 className="text-xl font-semibold">{lesson.title}</h2>
          <div className="text-sm text-slate-500">Category: {category}</div>
        </div>
        <div>
          <button onClick={goBack} className="px-3 py-1 rounded bg-slate-100">Back</button>
        </div>
      </div>

      <section className="mt-4">
        <h3 className="font-medium">Resources</h3>
        <div className="mt-2 grid gap-2">
          {lesson.resources.length === 0 && <div className="text-sm text-slate-500">No resources yet. Add YouTube links, PPT links, or notes below.</div>}
          {lesson.resources.map(r => (
            <div key={r.id} className="p-2 border rounded flex items-start gap-3">
              <div className="flex-1">
                <div className="font-semibold">{r.type.toUpperCase()}</div>
                <div className="text-sm text-slate-600 break-all">{r.url}</div>
                {r.note && <div className="text-sm text-slate-500">{r.note}</div>}
              </div>
              <div>
                {r.type === 'youtube' && <a href={r.url} target="_blank" rel="noreferrer" className="underline text-sm">Watch</a>}
                {r.type === 'ppt' && <a href={r.url} target="_blank" rel="noreferrer" className="underline text-sm">Open PPT</a>}
              </div>
            </div>
          ))}
        </div>
      </section>

      <section className="mt-4 border-t pt-4">
        <h3 className="font-medium">Add Resource</h3>
        <div className="mt-2 grid grid-cols-1 md:grid-cols-3 gap-2">
          <select value={resType} onChange={e => setResType(e.target.value)} className="p-2 border rounded">
            <option value="youtube">YouTube Link</option>
            <option value="ppt">PPT / Google Slides Link</option>
            <option value="note">Note / Article Link</option>
          </select>
          <input placeholder="URL or title" value={resUrl} onChange={e => setResUrl(e.target.value)} className="p-2 border rounded col-span-2 md:col-span-1" />
          <input placeholder="Short note (optional)" value={note} onChange={e => setNote(e.target.value)} className="p-2 border rounded md:col-span-2" />
          <div className="md:col-span-3">
            <button onClick={handleAdd} className="px-3 py-1 rounded bg-indigo-600 text-white">Add Resource</button>
          </div>
        </div>
      </section>

    </div>
  );
}

function QuizEditor({ lessons, onSave, onCancel }) {
  const [title, setTitle] = useState('');
  const [timeLimitMin, setTimeLimitMin] = useState(15);
  const [questions, setQuestions] = useState([]);

  const addQuestion = () => setQuestions(prev => [...prev, { id: 'q_' + Date.now(), type: 'mcq', prompt: '', options: ['', ''], correctIndex: 0, rationale: '' }]);
  const updateQuestion = (id, patch) => setQuestions(prev => prev.map(q => q.id === id ? { ...q, ...patch } : q));
  const removeQuestion = (id) => setQuestions(prev => prev.filter(q => q.id !== id));

  const save = () => {
    if (!title) return alert('Give quiz a title');
    if (questions.length === 0) return alert('Add at least one question');
    onSave({ title, timeLimitSec: timeLimitMin * 60, questions });
  };

  return (
    <div className="bg-white p-4 rounded shadow">
      <h2 className="text-xl font-semibold">Create Quiz</h2>
      <div className="mt-3 grid gap-2">
        <input placeholder="Quiz title" value={title} onChange={e => setTitle(e.target.value)} className="p-2 border rounded" />
        <div className="flex gap-2">
          <input type="number" value={timeLimitMin} onChange={e => setTimeLimitMin(Number(e.target.value))} className="p-2 border rounded w-32" />
          <div className="text-slate-500">minutes</div>
        </div>

        <div className="mt-2">
          <h3 className="font-medium">Questions</h3>
          <div className="space-y-3 mt-2">
            {questions.map(q => (
              <div key={q.id} className="p-3 border rounded">
                <div className="flex justify-between items-center mb-2">
                  <div className="font-semibold">{q.type.toUpperCase()}</div>
                  <div className="flex gap-2">
                    <select value={q.type} onChange={(e) => updateQuestion(q.id, { type: e.target.value })} className="p-1 border rounded">
                      <option value="mcq">MCQ</option>
                      <option value="short">Short Answer</option>
                    </select>
                    <button className="text-red-600" onClick={() => removeQuestion(q.id)}>Remove</button>
                  </div>
                </div>
                <input placeholder="Question prompt" value={q.prompt} onChange={(e) => updateQuestion(q.id, { prompt: e.target.value })} className="p-2 border rounded w-full" />
                {q.type === 'mcq' && (
                  <div className="mt-2">
                    <div className="text-sm text-slate-500">Options (mark correct):</div>
                    {q.options.map((opt, i) => (
                      <div key={i} className="flex gap-2 mt-1">
                        <input value={opt} onChange={(e) => {
                          const newOpts = [...q.options]; newOpts[i] = e.target.value; updateQuestion(q.id, { options: newOpts });
                        }} className="p-2 border rounded flex-1" />
                        <label className="flex items-center gap-1"><input type="radio" name={q.id + '_correct'} checked={q.correctIndex === i} onChange={() => updateQuestion(q.id, { correctIndex: i })} /> Correct</label>
                      </div>
                    ))}
                    <button className="mt-2 px-2 py-1 rounded bg-slate-100" onClick={() => updateQuestion(q.id, { options: [...q.options, ''] })}>Add option</button>
                  </div>
                )}
                <div className="mt-2">
                  <input placeholder="Rationale (explain answer)" value={q.rationale} onChange={(e) => updateQuestion(q.id, { rationale: e.target.value })} className="p-2 border rounded w-full" />
                </div>
              </div>
            ))}
            <div>
              <button className="px-3 py-1 rounded bg-indigo-600 text-white" onClick={addQuestion}>Add Question</button>
            </div>
          </div>
        </div>

        <div className="flex gap-2">
          <button className="px-3 py-1 rounded bg-emerald-600 text-white" onClick={save}>Save Quiz</button>
          <button className="px-3 py-1 rounded bg-slate-200" onClick={onCancel}>Cancel</button>
        </div>
      </div>
    </div>
  );
}

function QuizRunner({ quiz, onSave, onCancel }) {
  const [index, setIndex] = useState(0);
  const [answers, setAnswers] = useState({});
  const [timeLeft, setTimeLeft] = useState(quiz.timeLimitSec || 0);
  const [running, setRunning] = useState(!!quiz.timeLimitSec);
  const timerRef = useRef(null);

  useEffect(() => {
    if (!running) return;
    timerRef.current = setInterval(() => setTimeLeft(t => t - 1), 1000);
    return () => clearInterval(timerRef.current);
  }, [running]);

  useEffect(() => {
    if (timeLeft <= 0 && running) {
      clearInterval(timerRef.current);
      setRunning(false);
      submit();
    }
  }, [timeLeft, running]);

  const submit = () => {
    // grade MCQs / short answers heuristic
    const result = { total: quiz.questions.length, correct: 0, details: [] };
    quiz.questions.forEach((q, i) => {
      const given = answers[i];
      let ok = false;
      if (q.type === 'mcq') ok = given === q.correctIndex;
      else ok = (typeof given === 'string' && given.trim().length > 0); // short answer: accept non-empty
      if (ok) result.correct += 1;
      result.details.push({ index: i, ok, given, rationale: q.rationale });
    });
    onSave(result);
    alert(`Quiz submitted: ${result.correct}/${result.total}`);
  };

  if (!quiz) return (<div className="bg-white p-4 rounded shadow">Quiz not found. <button onClick={onCancel}>Back</button></div>);

  return (
    <div className="bg-white p-4 rounded shadow">
      <div className="flex items-center justify-between">
        <div>
          <h2 className="text-xl font-semibold">{quiz.title}</h2>
          <div className="text-sm text-slate-500">{quiz.questions.length} questions</div>
        </div>
        <div className="text-right">
          {quiz.timeLimitSec ? (
            <div className="text-sm">Time left: <strong>{formatTime(timeLeft)}</strong></div>
          ) : <div className="text-sm">No time limit</div>}
          <div className="mt-2 flex gap-2">
            <button className="px-2 py-1 rounded bg-slate-100" onClick={() => setRunning(!running)}>{running ? 'Pause' : 'Start'}</button>
            <button className="px-2 py-1 rounded bg-red-100" onClick={submit}>Submit</button>
          </div>
        </div>
      </div>

      <div className="mt-4">
        <QuestionView
          question={quiz.questions[index]}
          qIndex={index}
          onAnswer={(ans) => setAnswers(prev => ({ ...prev, [index]: ans }))}
          answer={answers[index]}
        />

        <div className="mt-4 flex justify-between">
          <div>
            <button className="px-3 py-1 rounded bg-slate-200" onClick={() => setIndex(i => Math.max(0, i - 1))}>Previous</button>
            <button className="ml-2 px-3 py-1 rounded bg-slate-200" onClick={() => setIndex(i => Math.min(quiz.questions.length - 1, i + 1))}>Next</button>
          </div>
          <div className="text-sm text-slate-500">Question {index + 1} / {quiz.questions.length}</div>
        </div>
      </div>

      <section className="mt-4 border-t pt-4">
        <h3 className="font-medium">Rationale & Results (after submission)</h3>
        <div className="text-sm text-slate-500">When you press submit, you'll get an overall score and each question's rationale will be saved to progress.</div>
      </section>
    </div>
  );
}

function QuestionView({ question, onAnswer, answer, qIndex }) {
  if (!question) return null;
  if (question.type === 'mcq') {
    return (
      <div>
        <div className="font-semibold">{question.prompt}</div>
        <div className="mt-2 grid gap-2">
          {question.options.map((opt, i) => (
            <label key={i} className={`p-2 border rounded cursor-pointer ${answer === i ? 'bg-slate-100' : ''}`}>
              <input type="radio" name={'q_' + qIndex} checked={answer === i} onChange={() => onAnswer(i)} /> <span className="ml-2">{opt}</span>
            </label>
          ))}
        </div>
      </div>
    );
  }
  return (
    <div>
      <div className="font-semibold">{question.prompt}</div>
      <textarea value={answer || ''} onChange={(e) => onAnswer(e.target.value)} className="mt-2 p-2 border rounded w-full" rows={4} />
    </div>
  );
}

// helpers
function formatTime(sec) {
  if (sec <= 0) return '00:00';
  const m = Math.floor(sec / 60); const s = sec % 60;
  return `${String(m).padStart(2, '0')}:${String(s).padStart(2, '0')}`;
}

function generateTwoWeekPlan() {
  // Simple rotating plan across categories — user can edit after importing
  const subjects = Object.keys(SAMPLE_LESSONS);
  const plan = [];
  const today = new Date();
  for (let d = 0; d < 14; d++) {
    const date = new Date(today); date.setDate(today.getDate() + d);
    const subject = subjects[d % subjects.length];
    const lessons = SAMPLE_LESSONS[subject];
    const pick = lessons[d % lessons.length];
    plan.push({ day: d + 1, date: date.toISOString().slice(0, 10), subject, lessonId: pick.id, lessonTitle: pick.title });
  }
  return plan;
}

export default App;
