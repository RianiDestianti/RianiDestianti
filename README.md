import React, { useState, useEffect } from 'react';
import { motion } from 'framer-motion';
import { Globe, Book, Code, Radio, Star, User, Mail, Heart } from 'lucide-react';

const InteractiveProfile = () => {
  const [isVisible, setIsVisible] = useState({
    about: false,
    skills: false,
    tech: false,
    currently: false
  });

  const [activeTab, setActiveTab] = useState('about');

  const codeString = `
class Developer {
    val name = "Riani Destianti"
    val education = "Software Engineering Student"
    val location = "Bandung, Indonesia"

    val interests = listOf(
        "Mobile Development",
        "Machine Learning",
        "Web Development"
    )
}`;

  const technologies = {
    Mobile: ["Flutter", "Kotlin", "React Native"],
    Backend: ["PHP", "Laravel", "MySQL"],
    Frontend: ["HTML5", "CSS3", "JavaScript", "Bootstrap"],
    Other: ["Python", "C#", "Arduino"]
  };

  return (
    <div className="max-w-4xl mx-auto p-6 bg-gray-50 rounded-lg shadow-xl">
      {/* Header Section with Floating Animation */}
      <motion.div 
        initial={{ y: -20, opacity: 0 }}
        animate={{ y: 0, opacity: 1 }}
        className="text-center mb-8"
      >
        <h1 className="text-4xl font-bold bg-gradient-to-r from-pink-500 to-purple-500 text-transparent bg-clip-text mb-4">
          Hi there, I'm Riani Destianti! 👋
        </h1>
        <motion.div 
          animate={{ y: [0, -10, 0] }}
          transition={{ duration: 2, repeat: Infinity }}
          className="text-xl text-gray-600"
        >
          Mobile App Development Enthusiast
        </motion.div>
      </motion.div>

      {/* Interactive Navigation */}
      <div className="flex justify-center space-x-4 mb-8">
        {['about', 'skills', 'tech', 'currently'].map((tab) => (
          <motion.button
            key={tab}
            whileHover={{ scale: 1.1 }}
            whileTap={{ scale: 0.95 }}
            className={`px-4 py-2 rounded-lg ${
              activeTab === tab 
                ? 'bg-purple-500 text-white' 
                : 'bg-gray-200 text-gray-700'
            }`}
            onClick={() => setActiveTab(tab)}
          >
            {tab.charAt(0).toUpperCase() + tab.slice(1)}
          </motion.button>
        ))}
      </div>

      {/* Content Sections */}
      <motion.div 
        className="bg-white p-6 rounded-lg shadow-lg"
        initial={{ opacity: 0, y: 20 }}
        animate={{ opacity: 1, y: 0 }}
        transition={{ duration: 0.5 }}
      >
        {activeTab === 'about' && (
          <motion.div
            initial={{ opacity: 0 }}
            animate={{ opacity: 1 }}
            transition={{ duration: 0.5 }}
          >
            <div className="bg-gray-800 text-gray-100 p-4 rounded-lg font-mono">
              <pre>{codeString}</pre>
            </div>
          </motion.div>
        )}

        {activeTab === 'skills' && (
          <motion.div
            initial={{ opacity: 0 }}
            animate={{ opacity: 1 }}
            className="space-y-4"
          >
            {Object.entries(technologies).map(([category, techs], index) => (
              <motion.div
                key={category}
                initial={{ x: -20, opacity: 0 }}
                animate={{ x: 0, opacity: 1 }}
                transition={{ delay: index * 0.1 }}
                className="mb-4"
              >
                <h3 className="text-xl font-bold mb-2">{category}</h3>
                <div className="flex flex-wrap gap-2">
                  {techs.map((tech) => (
                    <motion.span
                      key={tech}
                      whileHover={{ scale: 1.1 }}
                      className="px-3 py-1 bg-purple-100 text-purple-600 rounded-full"
                    >
                      {tech}
                    </motion.span>
                  ))}
                </div>
              </motion.div>
            ))}
          </motion.div>
        )}

        {activeTab === 'tech' && (
          <div className="grid grid-cols-2 md:grid-cols-3 gap-4">
            {['Flutter', 'Kotlin', 'React Native', 'Laravel', 'MySQL', 'Python'].map((tech) => (
              <motion.div
                key={tech}
                whileHover={{ scale: 1.05 }}
                className="p-4 bg-gradient-to-r from-purple-100 to-pink-100 rounded-lg text-center"
              >
                <h3 className="font-bold">{tech}</h3>
                <motion.div
                  animate={{ rotate: 360 }}
                  transition={{ duration: 2, repeat: Infinity, ease: "linear" }}
                  className="mt-2"
                >
                  <Code className="w-8 h-8 text-purple-500 mx-auto" />
                </motion.div>
              </motion.div>
            ))}
          </div>
        )}

        {activeTab === 'currently' && (
          <motion.div
            initial={{ opacity: 0 }}
            animate={{ opacity: 1 }}
            className="space-y-6"
          >
            <motion.div
              whileHover={{ scale: 1.02 }}
              className="p-4 bg-gradient-to-r from-purple-50 to-pink-50 rounded-lg"
            >
              <h3 className="text-xl font-bold mb-4">🌟 Currently</h3>
              <ul className="space-y-2">
                <motion.li
                  whileHover={{ x: 10 }}
                  className="flex items-center space-x-2"
                >
                  <Star className="text-yellow-500" />
                  <span>Learning Machine Learning & AI</span>
                </motion.li>
                <motion.li
                  whileHover={{ x: 10 }}
                  className="flex items-center space-x-2"
                >
                  <Globe className="text-blue-500" />
                  <span>Building Mobile Apps with Flutter</span>
                </motion.li>
                <motion.li
                  whileHover={{ x: 10 }}
                  className="flex items-center space-x-2"
                >
                  <Book className="text-green-500" />
                  <span>Studying Software Engineering</span>
                </motion.li>
              </ul>
            </motion.div>
          </motion.div>
        )}
      </motion.div>

      {/* Social Links */}
      <motion.div 
        className="mt-8 flex justify-center space-x-4"
        initial={{ y: 20, opacity: 0 }}
        animate={{ y: 0, opacity: 1 }}
        transition={{ delay: 0.5 }}
      >
        <motion.a
          href="https://www.instagram.com/rianidstiantii/"
          whileHover={{ scale: 1.1 }}
          className="p-2 bg-pink-500 text-white rounded-full"
        >
          <User className="w-6 h-6" />
        </motion.a>
        <motion.a
          href="https://www.linkedin.com/in/riani-destianti-70504a323/"
          whileHover={{ scale: 1.1 }}
          className="p-2 bg-blue-500 text-white rounded-full"
        >
          <Mail className="w-6 h-6" />
        </motion.a>
      </motion.div>

      {/* Footer */}
      <motion.div 
        className="mt-8 text-center text-gray-600"
        animate={{ y: [0, -5, 0] }}
        transition={{ duration: 2, repeat: Infinity }}
      >
        <p className="flex items-center justify-center">
          Made with <Heart className="w-4 h-4 mx-1 text-red-500" /> by Riani
        </p>
      </motion.div>
    </div>
  );
};

export default InteractiveProfile;
