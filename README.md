import React, { useState } from 'react';
import { Github, Linkedin, Facebook, Mail, ExternalLink, Code2, Briefcase, BookOpen } from 'lucide-react';

export default function Portfolio() {
  const [hoveredProject, setHoveredProject] = useState(null);
  const [hoveredSkill, setHoveredSkill] = useState(null);

  const projects = [
    {
      name: 'EduCoree',
      url: 'https://edu-coree.runasp.net/',
      status: 'Working on',
      description: 'منصة تعليمية متكاملة',
      icon: BookOpen,
      color: 'from-blue-500 to-cyan-500'
    },
    {
      name: 'Ijarify',
      url: 'https://ijarify.runasp.net/',
      status: 'Looking to collaborate',
      description: 'نظام إدارة الإيجارات',
      icon: Briefcase,
      color: 'from-purple-500 to-pink-500'
    },
    {
      name: 'Sana3y',
      url: 'https://snai3y.vercel.app/',
      status: 'Looking for help',
      description: 'منصة للحرفيين والصناعات',
      icon: Code2,
      color: 'from-orange-500 to-red-500'
    }
  ];

  const skills = [
    { name: 'Angular', category: 'Frontend', level: 95 },
    { name: 'C#/.NET', category: 'Backend', level: 98 },
    { name: 'TypeScript', category: 'Language', level: 90 },
    { name: 'SQL Server', category: 'Database', level: 92 },
    { name: 'React', category: 'Frontend', level: 75 },
    { name: 'Node.js', category: 'Backend', level: 70 },
    { name: 'Azure', category: 'Cloud', level: 80 },
    { name: 'Python', category: 'Language', level: 85 }
  ];

  const technologies = [
    'Angular', 'TypeScript', 'C#', '.NET', 'SQL Server', 'Azure', 'AWS',
    'Bootstrap', 'Tailwind', 'Git', 'Postman', 'Figma', 'Python', 'Pandas',
    'PyTorch', 'Scikit-learn', 'Oracle', 'JavaScript', 'HTML5', 'CSS3', 'Sass'
  ];

  return (
    <div className="min-h-screen bg-gradient-to-br from-slate-900 via-slate-800 to-slate-900 text-white overflow-x-hidden">
      <style>{`
        @import url('https://fonts.googleapis.com/css2?family=Sora:wght@300;400;600;700;800&family=DM+Sans:wght@400;500;700&display=swap');
        
        * {
          font-family: 'DM Sans', sans-serif;
        }
        
        h1, h2, h3, h4, h5, h6 {
          font-family: 'Sora', sans-serif;
        }

        @keyframes fadeInUp {
          from {
            opacity: 0;
            transform: translateY(30px);
          }
          to {
            opacity: 1;
            transform: translateY(0);
          }
        }

        @keyframes float {
          0%, 100% { transform: translateY(0px); }
          50% { transform: translateY(-20px); }
        }

        @keyframes glow {
          0%, 100% { box-shadow: 0 0 20px rgba(59, 130, 246, 0.5); }
          50% { box-shadow: 0 0 40px rgba(59, 130, 246, 0.8), 0 0 60px rgba(139, 92, 246, 0.6); }
        }

        .animate-fade-in-up {
          animation: fadeInUp 0.8s ease-out forwards;
        }

        .animate-float {
          animation: float 6s ease-in-out infinite;
        }

        .animate-glow {
          animation: glow 3s ease-in-out infinite;
        }

        .delay-100 { animation-delay: 0.1s; }
        .delay-200 { animation-delay: 0.2s; }
        .delay-300 { animation-delay: 0.3s; }
        .delay-400 { animation-delay: 0.4s; }
        .delay-500 { animation-delay: 0.5s; }

        .gradient-text {
          background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
          -webkit-background-clip: text;
          -webkit-text-fill-color: transparent;
          background-clip: text;
        }

        .tech-badge {
          transition: all 0.3s cubic-bezier(0.4, 0, 0.2, 1);
        }

        .tech-badge:hover {
          transform: translateY(-3px) scale(1.05);
        }

        .project-card {
          transition: all 0.4s cubic-bezier(0.4, 0, 0.2, 1);
        }

        .project-card:hover {
          transform: translateY(-8px);
        }

        .skill-bar {
          transition: width 1.5s cubic-bezier(0.4, 0, 0.2, 1);
        }

        .glass-effect {
          background: rgba(255, 255, 255, 0.05);
          backdrop-filter: blur(10px);
          border: 1px solid rgba(255, 255, 255, 0.1);
        }

        .bg-grid {
          background-image: 
            linear-gradient(rgba(255, 255, 255, 0.03) 1px, transparent 1px),
            linear-gradient(90deg, rgba(255, 255, 255, 0.03) 1px, transparent 1px);
          background-size: 50px 50px;
        }
      `}</style>

      {/* Animated Background Grid */}
      <div className="fixed inset-0 bg-grid opacity-40 pointer-events-none"></div>

      {/* Floating Orbs */}
      <div className="fixed top-20 left-10 w-72 h-72 bg-blue-500 rounded-full mix-blend-multiply filter blur-3xl opacity-20 animate-float"></div>
      <div className="fixed bottom-20 right-10 w-72 h-72 bg-purple-500 rounded-full mix-blend-multiply filter blur-3xl opacity-20 animate-float" style={{ animationDelay: '2s' }}></div>

      <div className="relative z-10 container mx-auto px-4 py-12 max-w-6xl">
        
        {/* Hero Section */}
        <div className="text-center mb-20 animate-fade-in-up">
          <div className="mb-6">
            <div className="w-32 h-32 mx-auto rounded-full bg-gradient-to-br from-blue-500 via-purple-500 to-pink-500 p-1 animate-glow">
              <div className="w-full h-full rounded-full bg-slate-900 flex items-center justify-center">
                <span className="text-5xl font-bold gradient-text">AR</span>
              </div>
            </div>
          </div>
          
          <h1 className="text-6xl md:text-7xl font-bold mb-4 bg-gradient-to-r from-blue-400 via-purple-400 to-pink-400 bg-clip-text text-transparent">
            Ahmed Samir Rady
          </h1>
          
          <p className="text-2xl md:text-3xl text-gray-300 mb-6 font-light">
            Full Stack .NET Developer
          </p>
          
          <div className="flex gap-4 justify-center mb-8">
            <a href="https://www.linkedin.com/in/ahmed-samir-388b90389/" 
               target="_blank"
               rel="noopener noreferrer"
               className="glass-effect p-4 rounded-full hover:bg-blue-500/20 transition-all duration-300 hover:scale-110">
              <Linkedin className="w-6 h-6" />
            </a>
            <a href="https://www.facebook.com/ahmed.samir.387021" 
               target="_blank"
               rel="noopener noreferrer"
               className="glass-effect p-4 rounded-full hover:bg-blue-500/20 transition-all duration-300 hover:scale-110">
              <Facebook className="w-6 h-6" />
            </a>
            <a href="mailto:arady6903@gmail.com"
               className="glass-effect p-4 rounded-full hover:bg-blue-500/20 transition-all duration-300 hover:scale-110">
              <Mail className="w-6 h-6" />
            </a>
          </div>

          <div className="flex gap-4 justify-center flex-wrap">
            <span className="glass-effect px-6 py-2 rounded-full text-sm">
              💬 Ask me about <span className="text-blue-400 font-semibold">Angular</span> & <span className="text-purple-400 font-semibold">.NET</span>
            </span>
            <span className="glass-effect px-6 py-2 rounded-full text-sm">
              🌱 Learning <span className="text-green-400 font-semibold">React</span> & <span className="text-yellow-400 font-semibold">Node.js</span>
            </span>
          </div>
        </div>

        {/* Projects Section */}
        <div className="mb-20 animate-fade-in-up delay-200">
          <h2 className="text-4xl font-bold mb-10 text-center">
            <span className="bg-gradient-to-r from-blue-400 to-purple-400 bg-clip-text text-transparent">
              Current Projects
            </span>
          </h2>
          
          <div className="grid md:grid-cols-3 gap-6">
            {projects.map((project, idx) => (
              <div
                key={idx}
                className="project-card glass-effect rounded-2xl p-6 cursor-pointer"
                onMouseEnter={() => setHoveredProject(idx)}
                onMouseLeave={() => setHoveredProject(null)}
              >
                <div className={`w-14 h-14 rounded-xl bg-gradient-to-br ${project.color} flex items-center justify-center mb-4`}>
                  <project.icon className="w-8 h-8 text-white" />
                </div>
                
                <h3 className="text-2xl font-bold mb-2">{project.name}</h3>
                <p className="text-sm text-gray-400 mb-3">{project.status}</p>
                <p className="text-gray-300 mb-4">{project.description}</p>
                
                <a 
                  href={project.url}
                  target="_blank"
                  rel="noopener noreferrer"
                  className={`inline-flex items-center gap-2 text-blue-400 hover:text-blue-300 transition-all ${
                    hoveredProject === idx ? 'translate-x-2' : ''
                  }`}
                >
                  Visit Project <ExternalLink className="w-4 h-4" />
                </a>
              </div>
            ))}
          </div>
        </div>

        {/* Skills Section */}
        <div className="mb-20 animate-fade-in-up delay-300">
          <h2 className="text-4xl font-bold mb-10 text-center">
            <span className="bg-gradient-to-r from-purple-400 to-pink-400 bg-clip-text text-transparent">
              Core Skills
            </span>
          </h2>
          
          <div className="grid md:grid-cols-2 gap-6">
            {skills.map((skill, idx) => (
              <div 
                key={idx}
                className="glass-effect rounded-xl p-6"
                onMouseEnter={() => setHoveredSkill(idx)}
                onMouseLeave={() => setHoveredSkill(null)}
              >
                <div className="flex justify-between items-center mb-3">
                  <div>
                    <h4 className="text-lg font-semibold">{skill.name}</h4>
                    <p className="text-sm text-gray-400">{skill.category}</p>
                  </div>
                  <span className="text-2xl font-bold text-blue-400">{skill.level}%</span>
                </div>
                
                <div className="w-full bg-slate-700 rounded-full h-2 overflow-hidden">
                  <div 
                    className={`skill-bar h-full bg-gradient-to-r from-blue-500 to-purple-500 rounded-full`}
                    style={{ 
                      width: hoveredSkill === idx || hoveredSkill === null ? `${skill.level}%` : '0%'
                    }}
                  ></div>
                </div>
              </div>
            ))}
          </div>
        </div>

        {/* Technologies Section */}
        <div className="mb-20 animate-fade-in-up delay-400">
          <h2 className="text-4xl font-bold mb-10 text-center">
            <span className="bg-gradient-to-r from-pink-400 to-orange-400 bg-clip-text text-transparent">
              Technologies & Tools
            </span>
          </h2>
          
          <div className="flex flex-wrap gap-3 justify-center">
            {technologies.map((tech, idx) => (
              <span
                key={idx}
                className="tech-badge glass-effect px-5 py-3 rounded-full text-sm font-medium hover:bg-gradient-to-r hover:from-blue-500/20 hover:to-purple-500/20 cursor-default"
              >
                {tech}
              </span>
            ))}
          </div>
        </div>

        {/* Contact Section */}
        <div className="text-center animate-fade-in-up delay-500">
          <div className="glass-effect rounded-2xl p-10 max-w-2xl mx-auto">
            <h2 className="text-3xl font-bold mb-4">Let's Connect!</h2>
            <p className="text-gray-300 mb-6">
              I'm always open to discussing new projects, creative ideas, or opportunities to be part of your visions.
            </p>
            <a 
              href="mailto:arady6903@gmail.com"
              className="inline-flex items-center gap-2 bg-gradient-to-r from-blue-500 to-purple-500 px-8 py-4 rounded-full font-semibold hover:shadow-lg hover:shadow-purple-500/50 transition-all duration-300 hover:scale-105"
            >
              <Mail className="w-5 h-5" />
              Get in Touch
            </a>
          </div>
        </div>

        {/* Footer */}
        <div className="mt-16 text-center text-gray-500 text-sm">
          <p>© 2024 Ahmed Samir Rady. Built with React & Tailwind CSS.</p>
        </div>
      </div>
    </div>
  );
}
