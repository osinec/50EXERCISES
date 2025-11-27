import React, { useState, useEffect } from 'react';
import { motion, useScroll, useSpring } from 'framer-motion';
import { Sun, Moon, Menu, X } from 'lucide-react';

const App = () => {
  const [darkMode, setDarkMode] = useState(false);
  const [mobileMenuOpen, setMobileMenuOpen] = useState(false);
  const [activeSection, setActiveSection] = useState('');

  // Citation system
  useEffect(() => {
    document.querySelectorAll('[data-ref]').forEach(el => {
      // Skip if already processed
      if (el.dataset.citationProcessed) return;
      
      const refData = el.getAttribute('data-ref');
      if (!refData?.trim()) return;

      // Parse format: "url|indexNumber" e.g., "https://example.com|1"
      const separatorIndex = refData.indexOf('|');
      if (separatorIndex === -1) return;
      
      const url = refData.substring(0, separatorIndex).trim();
      const indexNum = refData.substring(separatorIndex + 1).trim();

      // Only add citation if element has text content
      if (!el.textContent?.trim()) return;

      const btn = document.createElement('sup');
      btn.textContent = String(indexNum);
      
      Object.assign(btn.style, {
        fontSize: '8px', top: '1%', color: '#fff', cursor: 'pointer', fontWeight: 'bold',
        backgroundColor: '#0284c7', borderRadius: '50%', transition: 'all .2s',
        userSelect: 'none', minWidth: '18px', height: '18px', marginLeft: '2px',
        display: 'inline-flex', alignItems: 'center', justifyContent: 'center',
        boxShadow: '0 1px 3px rgba(0,0,0,.2)', fontFamily: 'system-ui,-apple-system,sans-serif',
        lineHeight: '1', verticalAlign: 'baseline', padding: '0 2px'
      });

      btn.onmouseenter = () => Object.assign(btn.style, { backgroundColor: '#0369a1', transform: 'scale(1.15)', boxShadow: '0 2px 6px rgba(0,0,0,.3)' });
      btn.onmouseleave = () => Object.assign(btn.style, { backgroundColor: '#0284c7', transform: 'scale(1)', boxShadow: '0 1px 3px rgba(0,0,0,.2)' });
      btn.onclick = e => { e.stopPropagation(); e.preventDefault(); window.open(url, '_blank'); };

      el.appendChild(btn);
      
      // Mark as processed
      el.dataset.citationProcessed = 'true';
    });
  }, []);

  const { scrollYProgress } = useScroll();
  const scaleX = useSpring(scrollYProgress, {
    stiffness: 100,
    damping: 30,
    restDelta: 0.001
  });

  const toggleDarkMode = () => {
    setDarkMode(!darkMode);
  };

  const scrollToSection = (id) => {
    const element = document.getElementById(id);
    if (element) {
      element.scrollIntoView({ behavior: 'smooth' });
      setActiveSection(id);
      setMobileMenuOpen(false);
    }
  };

  useEffect(() => {
    const handleScroll = () => {
      const sections = ['hero', 'microsoft-bob', 'apple-ipod', 'comparison', 'conclusion'];
      const current = sections.find(section => {
        const element = document.getElementById(section);
        if (element) {
          const rect = element.getBoundingClientRect();
          return rect.top <= 100 && rect.bottom >= 100;
        }
        return false;
      });
      if (current) setActiveSection(current);
    };

    window.addEventListener('scroll', handleScroll);
    return () => window.removeEventListener('scroll', handleScroll);
  }, []);

  return (
    <div className={`min-h-screen transition-colors duration-300 ${darkMode ? 'bg-gray-900 text-gray-100' : 'bg-white text-gray-900'}`}>
      {/* Progress bar */}
      <motion.div
        className="fixed top-0 left-0 right-0 h-1 bg-primary-500 transform-origin-left z-50"
        style={scaleX}
      />

      {/* Floating Header */}
      <header className={`fixed top-0 left-0 right-0 z-40 backdrop-blur-md transition-all duration-300 ${darkMode ? 'bg-gray-900/80' : 'bg-white/80'}`}>
        <div className="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
          <div className="flex items-center justify-between h-16">
            <div className="flex items-center">
              <h1 className={`text-xl font-bold ${darkMode ? 'text-white' : 'text-gray-900'}`}>История Технологий</h1>
            </div>
            
            {/* Desktop Navigation */}
            <nav className="hidden md:flex space-x-8">
              {[
                { id: 'hero', label: 'Главная' },
                { id: 'microsoft-bob', label: 'Microsoft Bob' },
                { id: 'apple-ipod', label: 'Apple iPod' },
                { id: 'comparison', label: 'Сравнение' },
                { id: 'conclusion', label: 'Выводы' }
              ].map((item) => (
                <button
                  key={item.id}
                  onClick={() => scrollToSection(item.id)}
                  className={`px-3 py-2 rounded-md text-sm font-medium transition-colors ${
                    activeSection === item.id
                      ? 'bg-blue-500 text-white'
                      : darkMode
                        ? 'text-gray-300 hover:text-white'
                        : 'text-gray-700 hover:text-gray-900'
                  }`}
                >
                  {item.label}
                </button>
              ))}
            </nav>
            
            <div className="flex items-center space-x-4">
              <button
                onClick={toggleDarkMode}
                className={`p-2 rounded-full ${darkMode ? 'bg-gray-700 text-yellow-300' : 'bg-gray-200 text-gray-700'}`}
              >
                {darkMode ? <Sun size={20} /> : <Moon size={20} />}
              </button>
              
              {/* Mobile menu button */}
              <button
                onClick={() => setMobileMenuOpen(!mobileMenuOpen)}
                className="md:hidden p-2 rounded-md"
              >
                {mobileMenuOpen ? <X size={24} /> : <Menu size={24} />}
              </button>
            </div>
          </div>
        </div>
        
        {/* Mobile Navigation */}
        {mobileMenuOpen && (
          <div className={`md:hidden ${darkMode ? 'bg-gray-800' : 'bg-gray-100'} px-2 pt-2 pb-3 space-y-1`}>
            {[
              { id: 'hero', label: 'Главная' },
              { id: 'microsoft-bob', label: 'Microsoft Bob' },
              { id: 'apple-ipod', label: 'Apple iPod' },
              { id: 'comparison', label: 'Сравнение' },
              { id: 'conclusion', label: 'Выводы' }
            ].map((item) => (
              <button
                key={item.id}
                onClick={() => scrollToSection(item.id)}
                className={`block px-3 py-2 rounded-md text-base font-medium w-full text-left ${
                  activeSection === item.id
                    ? 'bg-blue-500 text-white'
                    : darkMode
                      ? 'text-gray-300 hover:text-white'
                      : 'text-gray-700 hover:text-gray-900'
                }`}
              >
                {item.label}
              </button>
            ))}
          </div>
        )}
      </header>

      {/* Hero Section */}
      <section id="hero" className="pt-24 pb-16">
        <div className="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
          <div className="text-center">
            <motion.h1 
              initial={{ opacity: 0, y: 20 }}
              animate={{ opacity: 1, y: 0 }}
              className={`text-4xl md:text-6xl font-bold mb-6 ${darkMode ? 'text-white' : 'text-gray-900'}`}
            >
              История провала Microsoft Bob и успеха Apple iPod
            </motion.h1>
            <motion.p 
              initial={{ opacity: 0, y: 20 }}
              animate={{ opacity: 1, y: 0 }}
              transition={{ delay: 0.1 }}
              className={`text-xl mb-8 max-w-3xl mx-auto ${darkMode ? 'text-gray-300' : 'text-gray-600'}`}
            >
              Исследование двух контрастных кейсов в истории разработки потребительских технологий, демонстрирующих, 
              как ясность видения продукта важнее объёма данных или сложности реализации
            </motion.p>
          </div>
        </div>
      </section>

      {/* Microsoft Bob Section */}
      <section id="microsoft-bob" className="py-16">
        <div className="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
          <motion.div
            initial={{ opacity: 0, y: 20 }}
            whileInView={{ opacity: 1, y: 0 }}
            viewport={{ once: true }}
            className="mb-12"
          >
            <h2 className={`text-3xl font-bold mb-8 ${darkMode ? 'text-white' : 'text-gray-900'}`}>
              Microsoft Bob: Провал в интерфейсном дизайне
            </h2>
            
            <img 
              src="https://cdn.qwenlm.ai/b8201c09-11d7-4345-8f4c-f612f5f174fc/fe235999-1bec-4c5e-a255-55549bfdb83a/03ce5852-9ac8-47f0-a945-c503fead9a75.png?key=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJyZXNvdXJjZV91c2VyX2lkIjoiYjgyMDFjMDktMTFkNy00MzQ1LThmNGMtZjYxMmY1ZjE3NGZjIiwicmVzb3VyY2VfaWQiOiJmZTIzNTk5OS0xYmVjLTRjNWUtYTI1NS01NTU0OWJmZGI4M2EiLCJyZXNvdXJjZV9jaGF0X2lkIjpudWxsfQ.ZQS63_5yAlyK0o6t_kkhNt78pc_yLq_wE5PKwmCqSLE" 
              alt="Иллюстрация интерфейса Microsoft Bob с виртуальным домом, комнатами и персонажем Rover собакой. Изображение выполнено в ярких, но устаревших цветах с элементами 90-х годов. На переднем плане видны комнаты с различными объектами, которые представляют собой приложения Windows. Стиль интерфейса напоминает детские обучающие программы с卡通-стилистикой и большими кнопками. Фон выполнен в теплых тонах с элементами деревянной мебели и домашней обстановки."
              className="w-full rounded-xl shadow-lg mb-8"
              data-ref="https://thehustle.co/news/why-though-microsoft-s-user-interface-that-only-kids-liked|35"
            />
            
            <div className="grid md:grid-cols-2 gap-8">
              <div>
                <h3 className={`text-2xl font-semibold mb-4 ${darkMode ? 'text-white' : 'text-gray-900'}`}>
                  Концепция и разработка
                </h3>
                <p className={`${darkMode ? 'text-gray-300' : 'text-gray-600'} mb-4`} data-ref="https://technologizer.com/2010/03/29/bob-and-beyond-a-microsoft-insider-remembers/index.html|4">
                  Microsoft Bob был выпущен в марте 1995 года как альтернативный интерфейс для Windows 3.1, 
                  разработанный для упрощения использования компьютеров новичками через виртуальную домашнюю 
                  среду с персонажами-проводниками, такими как 'Bob' и анимированные персонажи.
                </p>
                <p className={`${darkMode ? 'text-gray-300' : 'text-gray-600'} mb-4`} data-ref="https://www.youtube.com/watch?v=utjh8R-yedk|29">
                  Проект был разработан командой, которая выросла с трех до 35 человек, включая Мелинду Гейтс 
                  в качестве менеджера по маркетингу, и был задуман Барри Линеттом и Керен Фрайс, которые 
                  ранее работали над Microsoft Publisher.
                </p>
              </div>
              
              <div>
                <h3 className={`text-2xl font-semibold mb-4 ${darkMode ? 'text-white' : 'text-gray-900'}`}>
                  Причины провала
                </h3>
                <p className={`${darkMode ? 'text-gray-300' : 'text-gray-600'} mb-4`} data-ref="https://www.makeuseof.com/microsoft-bob-still-microsoft-most-awkward-invention/|8">
                  Пользователи находили его медленнее, более запутанным и раздражающим, чем стандартный Windows, 
                  из-за избыточной визуальной перегруженности и слащавого дизайна.
                </p>
                <p className={`${darkMode ? 'text-gray-300' : 'text-gray-600'} mb-4`} data-ref="https://www.youtube.com/watch?v=LgkgG8hQFts|38">
                  Microsoft Bob требовал 8 МБ оперативной памяти, что было высоким требованием для того времени, 
                  когда 4 МБ оперативной памяти было более распространено.
                </p>
              </div>
            </div>
            
            <div className="mt-8 p-6 rounded-lg" style={{ backgroundColor: darkMode ? '#374151' : '#f3f4f6' }}>
              <h3 className={`text-xl font-semibold mb-4 ${darkMode ? 'text-white' : 'text-gray-900'}`}>
                Последствия провала
              </h3>
              <p className={`${darkMode ? 'text-gray-300' : 'text-gray-600'} mb-4`} data-ref="https://technologizer.com/2010/03/29/bob-and-beyond-a-microsoft-insider-remembers/index.html|4">
                Провал Microsoft Bob привел к длительному негативному влиянию на дизайн пользовательского 
                интерфейса, включая создание Клиппи (помощника Office), который унаследовал вмешательства и 
                осуждающее поведение Боба.
              </p>
              <p className={`${darkMode ? 'text-gray-300' : 'text-gray-600'}`} data-ref="https://thehustle.co/news/why-though-microsoft-s-user-interface-that-only-kids-liked|35">
                Дизайнер Винсент Коннэре создал Comic Sans для использования в пузырях речи Rover, потому что 
                формальный Times New Roman был неуместен, однако шрифт не был готов к запуску Боба и вместо 
                этого дебютировал в более позднем пакете шрифтов.
              </p>
            </div>
          </motion.div>
        </div>
      </section>

      {/* Apple iPod Section */}
      <section id="apple-ipod" className="py-16">
        <div className="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
          <motion.div
            initial={{ opacity: 0, y: 20 }}
            whileInView={{ opacity: 1, y: 0 }}
            viewport={{ once: true }}
            className="mb-12"
          >
            <h2 className={`text-3xl font-bold mb-8 ${darkMode ? 'text-white' : 'text-gray-900'}`}>
              Apple iPod: Успех в минимализме
            </h2>
            
            <img 
              src="https://cdn.qwenlm.ai/b8201c09-11d7-4345-8f4c-f612f5f174fc/fe235999-1bec-4c5e-a255-55549bfdb83a/1734ff93-f553-4d6b-9465-9250432e9369.png?key=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJyZXNvdXJjZV91c2VyX2lkIjoiYjgyMDFjMDktMTFkNy00MzQ1LThmNGMtZjYxMmY1ZjE3NGZjIiwicmVzb3VyY2VfaWQiOiJmZTIzNTk5OS0xYmVjLTRjNWUtYTI1NS01NTU0OWJmZGI4M2EiLCJyZXNvdXJjZV9jaGF0X2lkIjpudWxsfQ.ZQS63_5yAlyK0o6t_kkhNt78pc_yLq_wE5PKwmCqSLE" 
              alt="Коллекция iPod разных поколений на белом фоне с акцентом на дизайн. Изображение показывает оригинальный iPod, iPod mini, iPod nano и iPod touch, расположенные в линию. Все устройства выполнены в белом и серебристом цвете с характерным колесом прокрутки. На заднем плане видна упрощенная схема, показывающая интеграцию с iTunes. Цветовая палитра чистая и минималистичная, подчеркивающая эстетику Apple. Каждое устройство имеет четкие линии и минимальное количество элементов управления."
              className="w-full rounded-xl shadow-lg mb-8"
              data-ref="https://www.apple.com/newsroom/2001/10/23Apple-Presents-iPod/|9"
            />
            
            <div className="grid md:grid-cols-2 gap-8">
              <div>
                <h3 className={`text-2xl font-semibold mb-4 ${darkMode ? 'text-white' : 'text-gray-900'}`}>
                  Концепция и запуск
                </h3>
                <p className={`${darkMode ? 'text-gray-300' : 'text-gray-600'} mb-4`} data-ref="https://www.apple.com/newsroom/2001/10/23Apple-Presents-iPod/|9">
                  Apple представила iPod 23 октября 2001 года как прорывной MP3-проигрыватель, способный 
                  хранить до 1000 песен в формате CD-качества в устройстве весом 6,5 унций.
                </p>
                <p className={`${darkMode ? 'text-gray-300' : 'text-gray-600'} mb-4`} data-ref="https://www.theguardian.com/music/2021/oct/23/20-years-of-the-ipod-how-music-and-tech-new-era-steve-jobs|10">
                  iPod был запущен в октябре 2001 года, когда музыкальная индустрия находилась в кризисе 
                  из-за цифрового пиратства; он помог создать легальный цифровой музыкальный рынок и 
                  трансформировал Apple в доминирующую технологическую компанию.
                </p>
              </div>
              
              <div>
                <h3 className={`text-2xl font-semibold mb-4 ${darkMode ? 'text-white' : 'text-gray-900'}`}>
                  Ключевые особенности
                </h3>
                <p className={`${darkMode ? 'text-gray-300' : 'text-gray-600'} mb-4`} data-ref="https://www.apple.com/newsroom/2001/10/23Apple-Presents-iPod/|9">
                  Устройство имело 5 ГБ жесткий диск, подключение FireWire для быстрой передачи данных 
                  (10 секунд на CD, менее 10 минут для 1000 песен), 10 часов работы от батареи и 
                  автоматическую синхронизацию с iTunes.
                </p>
                <p className={`${darkMode ? 'text-gray-300' : 'text-gray-600'} mb-4`} data-ref="https://www.futureplatforms.com/insights/death-of-the-ipod-and-why-its-legacy-lives-on|53">
                  iPod не был первым MP3-проигрывателем, но преуспел благодаря уникальному дизайну и 
                  простоте использования, что привлекло пользователей от компак-дисков и конкурирующих 
                  MP3-проигрывателей.
                </p>
              </div>
            </div>
            
            <div className="mt-8 p-6 rounded-lg" style={{ backgroundColor: darkMode ? '#374151' : '#f3f4f6' }}>
              <h3 className={`text-xl font-semibold mb-4 ${darkMode ? 'text-white' : 'text-gray-900'}`}>
                Влияние на рынок
              </h3>
              <p className={`${darkMode ? 'text-gray-300' : 'text-gray-600'} mb-4`} data-ref="https://www.backmarket.com/en-us/c/tech-education/history-of-the-ipod?srsltid=AfmBOooeMd1aIaFpBBM-YKlZUivQxeO86PU8V48m42PRuKdZPax0GM5j|24">
                К 2008 году Apple продала 54,8 миллиона iPod'ов, а к 2007 году iPod'ы составляли 25% 
                общих продаж Apple. В пике iPod имел более 90% рынка MP3-проигрывателей на основе 
                жестких дисков.
              </p>
              <p className={`${darkMode ? 'text-gray-300' : 'text-gray-600'}`} data-ref="https://www.youtube.com/watch?v=UDLaZK171OA|22">
                В конечном итоге iPod был отменен в мае 2022 года, что ознаменовало конец эры iPod, 
                но его влияние на дизайн и подход к потребительской электронике продолжает ощущаться.
              </p>
            </div>
          </motion.div>
        </div>
      </section>

      {/* Comparison Section */}
      <section id="comparison" className="py-16">
        <div className="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
          <motion.div
            initial={{ opacity: 0, y: 20 }}
            whileInView={{ opacity: 1, y: 0 }}
            viewport={{ once: true }}
            className="mb-12"
          >
            <h2 className={`text-3xl font-bold mb-8 ${darkMode ? 'text-white' : 'text-gray-900'}`}>
              Сравнительный анализ: Microsoft Bob против Apple iPod
            </h2>
            
            <div className="grid md:grid-cols-2 gap-8 mb-8">
              <div className={`p-6 rounded-lg ${darkMode ? 'bg-gray-800' : 'bg-blue-50'}`}>
                <h3 className={`text-2xl font-semibold mb-4 ${darkMode ? 'text-blue-400' : 'text-blue-600'}`}>
                  Microsoft Bob
                </h3>
                <ul className={`space-y-2 ${darkMode ? 'text-gray-300' : 'text-gray-700'}`}>
                  <li className="flex items-start">
                    <span className={`mr-2 ${darkMode ? 'text-red-400' : 'text-red-600'}`}>•</span>
                    <span data-ref="https://medium.com/design-bootcamp/7-biggest-ux-fails-by-big-companies-a404c6c5bff6|48">Избыточный интерфейс с виртуальным домом</span>
                  </li>
                  <li className="flex items-start">
                    <span className={`mr-2 ${darkMode ? 'text-red-400' : 'text-red-600'}`}>•</span>
                    <span data-ref="https://www.youtube.com/watch?v=LgkgG8hQFts|38">Воспринимался как снисходительный и детский</span>
                  </li>
                  <li className="flex items-start">
                    <span className={`mr-2 ${darkMode ? 'text-red-400' : 'text-red-600'}`}>•</span>
                    <span data-ref="https://www.youtube.com/watch?v=utjh8R-yedk|29">Высокие системные требования для своего времени</span>
                  </li>
                  <li className="flex items-start">
                    <span className={`mr-2 ${darkMode ? 'text-red-400' : 'text-red-600'}`}>•</span>
                    <span data-ref="https://technologizer.com/2010/03/29/bob-and-beyond-a-microsoft-insider-remembers/index.html|4">Неадекватная сложность для упрощения задач</span>
                  </li>
                  <li className="flex items-start">
                    <span className={`mr-2 ${darkMode ? 'text-red-400' : 'text-red-600'}`}>•</span>
                    <span data-ref="https://www.makeuseof.com/microsoft-bob-still-microsoft-most-awkward-invention/|8">Провал после менее чем года на рынке</span>
                  </li>
                </ul>
              </div>
              
              <div className={`p-6 rounded-lg ${darkMode ? 'bg-gray-800' : 'bg-green-50'}`}>
                <h3 className={`text-2xl font-semibold mb-4 ${darkMode ? 'text-green-400' : 'text-green-600'}`}>
                  Apple iPod
                </h3>
                <ul className={`space-y-2 ${darkMode ? 'text-gray-300' : 'text-gray-700'}`}>
                  <li className="flex items-start">
                    <span className={`mr-2 ${darkMode ? 'text-green-400' : 'text-green-600'}`}>•</span>
                    <span data-ref="https://www.apple.com/newsroom/2001/10/23Apple-Presents-iPod/|9">Минималистичный дизайн с колесом прокрутки</span>
                  </li>
                  <li className="flex items-start">
                    <span className={`mr-2 ${darkMode ? 'text-green-400' : 'text-green-600'}`}>•</span>
                    <span data-ref="https://www.futureplatforms.com/insights/death-of-the-ipod-and-why-its-legacy-lives-on|53">Четкое ценовое предложение: 1000 песен в кармане</span>
                  </li>
                  <li className="flex items-start">
                    <span className={`mr-2 ${darkMode ? 'text-green-400' : 'text-green-600'}`}>•</span>
                    <span data-ref="https://medium.com/@tinaphm7/evolution-of-ipod-e951dfa16e63|56">Интеграция с iTunes для простого управления музыкой</span>
                  </li>
                  <li className="flex items-start">
                    <span className={`mr-2 ${darkMode ? 'text-green-400' : 'text-green-600'}`}>•</span>
                    <span data-ref="https://twit.tv/posts/tech/ipods-23rd-anniversary-looking-back-device-saved-apple|55">Интуитивный интерфейс без руководства пользователя</span>
                  </li>
                  <li className="flex items-start">
                    <span className={`mr-2 ${darkMode ? 'text-green-400' : 'text-green-600'}`}>•</span>
                    <span data-ref="https://www.backmarket.com/en-us/c/tech-education/history-of-the-ipod?srsltid=AfmBOooeMd1aIaFpBBM-YKlZUivQxeO86PU8V48m42PRuKdZPax0GM5j|24">Более 400 миллионов проданных устройств</span>
                  </li>
                </ul>
              </div>
            </div>
            
            <div className={`p-6 rounded-lg ${darkMode ? 'bg-gray-800' : 'bg-gray-100'}`}>
              <h3 className={`text-2xl font-semibold mb-4 ${darkMode ? 'text-white' : 'text-gray-900'}`}>
                Ключевые различия в подходе
              </h3>
              <p className={`${darkMode ? 'text-gray-300' : 'text-gray-700'} mb-4`} data-ref="https://chep2m.medium.com/creative-nomad-vs-ipod-a-case-study-f008b4d9bc40|25">
                Microsoft Bob был разработан с инженерным подходом, сосредоточенным на технических 
                возможностях, в то время как Apple iPod был разработан с пользовательским подходом, 
                сосредоточенным на решении реальных проблем пользователей.
              </p>
              <p className={`${darkMode ? 'text-gray-300' : 'text-gray-700'}`} data-ref="https://www.linkedin.com/pulse/farewell-ipod-learn-from-apples-customer-experience-ian-brookes-frsa|45">
                Apple приняла подход 'customer-backward': начиная с вопроса 'Какие невероятные 
                преимущества мы можем дать клиенту?', а не с доступных технологий. Это привело к 
                созданию первого трансформационного пользовательского опыта в портативной музыке.
              </p>
            </div>
          </motion.div>
        </div>
      </section>

      {/* Conclusion Section */}
      <section id="conclusion" className="py-16">
        <div className="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
          <motion.div
            initial={{ opacity: 0, y: 20 }}
            whileInView={{ opacity: 1, y: 0 }}
            viewport={{ once: true }}
            className="mb-12"
          >
            <h2 className={`text-3xl font-bold mb-8 ${darkMode ? 'text-white' : 'text-gray-900'}`}>
              Выводы: Контроль рождается из ясности, а не из объема данных
            </h2>
            
            <div className={`p-8 rounded-lg ${darkMode ? 'bg-gray-800' : 'bg-indigo-50'}`}>
              <p className={`text-lg mb-6 ${darkMode ? 'text-gray-300' : 'text-gray-700'}`} data-ref="https://blog.codinghorror.com/the-only-truly-failed-project/|2">
                Основной урок из этих двух случаев заключается в том, что 'единственный действительно 
                неудачный проект - это тот, где вы ничего не узнали по пути', подчеркивая, что обучение 
                и рост важнее краткосрочного успеха или неудачи в разработке технологий.
              </p>
              
              <div className="grid md:grid-cols-3 gap-6 mb-6">
                <div className={`p-4 rounded ${darkMode ? 'bg-gray-700' : 'bg-white'}`}>
                  <h4 className={`font-semibold mb-2 ${darkMode ? 'text-blue-400' : 'text-blue-600'}`}>
                    Ясность видения
                  </h4>
                  <p className={`${darkMode ? 'text-gray-300' : 'text-gray-700'}`} data-ref="https://www.linkedin.com/pulse/farewell-ipod-learn-from-apples-customer-experience-ian-brookes-frsa|45">
                    Apple сосредоточилась на четком видении: поместить 1000 песен в карман, 
                    в то время как Microsoft попыталась решить слишком много задач одновременно.
                  </p>
                </div>
                
                <div className={`p-4 rounded ${darkMode ? 'bg-gray-700' : 'bg-white'}`}>
                  <h4 className={`font-semibold mb-2 ${darkMode ? 'text-green-400' : 'text-green-600'}`}>
                    Пользовательский опыт
                  </h4>
                  <p className={`${darkMode ? 'text-gray-300' : 'text-gray-700'}`} data-ref="https://www.brandvm.com/post/simplicity-apple-ipod-marketing-impact|27">
                    iPod был разработан с акцентом на простоту и эмоциональную связь, 
                    а не на технические характеристики, что отличало его от конкурентов.
                  </p>
                </div>
                
                <div className={`p-4 rounded ${darkMode ? 'bg-gray-700' : 'bg-white'}`}>
                  <h4 className={`font-semibold mb-2 ${darkMode ? 'text-purple-400' : 'text-purple-600'}`}>
                    Интеграция экосистемы
                  </h4>
                  <p className={`${darkMode ? 'text-gray-300' : 'text-gray-700'}`} data-ref="https://medium.com/@tinaphm7/evolution-of-ipod-e951dfa16e63|56">
                    Успех iPod был результатом интеграции аппаратного обеспечения, программного 
                    обеспечения и сервисов, создавая замкнутую экосистему.
                  </p>
                </div>
              </div>
              
              <p className={`${darkMode ? 'text-gray-300' : 'text-gray-700'}`} data-ref="https://www.youtube.com/watch?v=UDLaZK171OA|22">
                Эти два случая показывают, что ясность видения продукта важнее объема данных или 
                сложности реализации. Microsoft Bob был технически сложным, но не имел четкого 
                понимания потребностей пользователей, в то время как Apple iPod был простым, 
                но решал реальную проблему эффективно.
              </p>
            </div>
          </motion.div>
        </div>
      </section>

      {/* Footer */}
      <footer className={`py-8 ${darkMode ? 'bg-gray-800' : 'bg-gray-100'}`}>
        <div className="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
          <p className={`text-center ${darkMode ? 'text-gray-400' : 'text-gray-600'}`}>
            Исследование истории технологий: Microsoft Bob и Apple iPod
          </p>
        </div>
      </footer>
    </div>
  );
};

export default App;
