import { motion } from "framer-motion";
import { useEffect, useRef, useState } from "react";

export default function BirthdayMemoryWebsite() {
  const sectionRefs = useRef([]);
  const [showLoader, setShowLoader] = useState(true);

  useEffect(() => {
    const timer = setTimeout(() => {
      setShowLoader(false);
    }, 3500);

    return () => clearTimeout(timer);
  }, []);
  const slides = [
    {
      title: "HAPPY BIRTHDAY 🎂",
      text: "To my cutest and craziest bestfriend — today is your special day and I just want to see you smile forever 💖",
    },
    {
      title: "Hey Birthday Star 😄",
      text: "Who brings the most positive vibes, endless laughter, and happiness everywhere? Yup, that's YOU ✨",
    },
    {
      title: "Bestfriend Check 🌸",
      text: "Who listens to every random story, supports like family, and makes life more fun? Obviously YOU 💕",
    },
    {
      title: "Final Birthday Question 🎈",
      text: "Who deserves unlimited cake, gifts, happiness, and the best birthday ever today? 100% YOU Bestie 🎂💖",
    },
  ];

  const surpriseQuotes = [
    "You are an amazing friend forever 🌸",
    "Every memory with you feels special ✨",
    "Your smile makes every day brighter 🌸",
    "Friendship becomes more fun when you are around 🎂",
  ];

  const floatingHearts = Array.from({ length: 30 }, (_, i) => ({
    id: i,
    left: Math.random() * 100,
    duration: 4 + Math.random() * 6,
    delay: Math.random() * 5,
  }));

  const friendshipPromises = [
    "I promise to always make you smile 😄",
    "I promise to stay beside you forever 💖",
    "I promise to protect our memories ✨",
    "I promise to annoy you forever 😂",
    "I promise to support your dreams 🌸",
    "I promise to celebrate every birthday with love 🎂",
  ];

  const timelineMoments = [
    {
      year: "First Meet",
      desc: "The day life became more beautiful because of you ✨",
    },
    {
      year: "Best Memories",
      desc: "Every laugh and joke became unforgettable 💕",
    },
    {
      year: "Today",
      desc: "Celebrating the most special bestfriend ever 🎂",
    },
  ];

  const cakeMessages = [
    "May your life always stay sweet like birthday cake 🎂",
    "Today is your day to smile without limits 💖",
    "Bestfriends like you are rare and precious ✨",
    "You deserve happiness bigger than the universe 🌌",
  ];

  const funFacts = [
    "You are officially the CEO of being adorable 😂",
    "Your smile has magical powers 🌸",
    "You make boring days beautiful 💕",
    "Friendship with you feels like a movie 🎬",
  ];

  const letterParagraphs = [
    "Dear Bestfriend, thank you for being the light in my darkest moments and the reason behind my happiest memories.",
    "Every laugh, every joke, and every random conversation with you became a memory I never want to lose.",
    "On your birthday, I just want you to know that you are deeply appreciated, loved, and celebrated.",
  ];

  const starMessages = [
    "You shine brighter than every star ✨",
    "A bestfriend like you is a blessing 🌟",
    "Your happiness matters the most 💖",
    "You make life colorful like a rainbow 🌈",
    "This birthday is all about YOU 🎂",
  ];

  const birthdayReasons = [
    "Because you always support me 🤝",
    "Because your smile heals everything 🌸",
    "Because every memory with you is priceless 📸",
    "Because you are truly one in a million ✨",
  ];

  const memories = [
    {
      title: "The First Smile",
      text: "Every moment with you became brighter from the very first smile you gave me.",
      emoji: "✨",
    },
    {
      title: "Late Night Talks",
      text: "The endless conversations, random jokes, and comfort in your voice are unforgettable.",
      emoji: "🌙",
    },
    {
      title: "Our Best Adventure",
      text: "Every little memory with you feels like a movie scene I never want to end.",
      emoji: "🎡",
    },
    {
      title: "Your Happiness",
      text: "Seeing you smile has always been my favorite thing in the world.",
      emoji: "💖",
    },
  ];

  return (
    <div className="min-h-screen overflow-x-hidden bg-gradient-to-br from-[#ffd6e8] via-[#ffeef5] to-[#fff5d9] relative font-sans scroll-smooth">
      {/* Opening Loader Screen */}
      {showLoader && (
        <div className="fixed inset-0 z-[999] flex items-center justify-center bg-gradient-to-br from-rose-500 via-pink-400 to-orange-300 animate-pulse transition-all duration-1000">
          <div className="text-center px-6">
            <h1 className="text-6xl md:text-8xl font-black text-white drop-shadow-2xl tracking-widest animate-bounce">
              HAPPY
            </h1>
            <h1 className="text-6xl md:text-8xl font-black text-white drop-shadow-2xl tracking-widest mt-4 animate-pulse">
              BIRTHDAY 🎂
            </h1>

            <p className="mt-8 text-2xl text-white font-semibold animate-bounce">
              A Special Surprise Is Waiting ✨
            </p>
          </div>
        </div>
      )}
      {/* Custom Animations */}
      <style>{`
        @keyframes floatUp {
          0% {
            transform: translateY(100vh) scale(0.8);
            opacity: 0;
          }
          100% {
            transform: translateY(-120vh) scale(1.1);
            opacity: 1;
          }
        }

        @keyframes glow {
          0% {
            box-shadow: 0 0 10px rgba(255,255,255,0.4);
          }
          50% {
            box-shadow: 0 0 50px rgba(255,255,255,0.9);
          }
          100% {
            box-shadow: 0 0 10px rgba(255,255,255,0.4);
          }
        }

        @keyframes rotateSlow {
          0% {
            transform: rotate(0deg);
          }
          100% {
            transform: rotate(360deg);
          }
        }

        @keyframes fadeSlide {
          0% {
            opacity: 0;
            transform: translateY(50px);
          }
          100% {
            opacity: 1;
            transform: translateY(0px);
          }
        }

        .balloonFloat {
          animation: floatUp linear infinite;
        }

        .glowEffect {
          animation: glow 3s infinite ease-in-out;
        }

        .rotateSlow {
          animation: rotateSlow 30s linear infinite;
        }

        .arrivalAnimation {
          animation: fadeSlide 2s ease forwards;
        }
      `}</style>
      {/* Background Glow Circles */}
      <div className="absolute top-10 left-10 w-72 h-72 rounded-full bg-pink-300/30 blur-3xl rotateSlow"></div>
      <div className="absolute bottom-10 right-10 w-96 h-96 rounded-full bg-rose-300/30 blur-3xl rotateSlow"></div>

      {/* Floating Hearts */}
      <div className="absolute inset-0 overflow-hidden pointer-events-none z-0">
        {floatingHearts.map((heart) => (
          <div
            key={heart.id}
            className="absolute text-pink-400 text-3xl animate-bounce"
            style={{
              left: `${heart.left}%`,
              bottom: `-10%`,
              animationDuration: `${heart.duration}s`,
              animationDelay: `${heart.delay}s`,
            }}
          >
            💖
          </div>
        ))}
      </div>

      {/* Floating Balloons */}
      <div className="absolute inset-0 overflow-hidden pointer-events-none">
        {[...Array(15)].map((_, i) => (
          <div
            key={i}
            className="absolute balloonFloat"
            style={{
              left: `${Math.random() * 100}%`,
              top: `120%`,
              animationDuration: `${3 + Math.random() * 5}s`,
            }}
          >
            <div className="w-16 h-20 rounded-full bg-pink-400 opacity-70 relative shadow-xl">
              <div className="absolute bottom-[-40px] left-1/2 w-[2px] h-10 bg-gray-500"></div>
            </div>
          </div>
        ))}
      </div>

      {/* Slide Sections */}
      {slides.map((slide, index) => (
        <section
          ref={(el) => {
            sectionRefs.current[index] = el;
          }}
          key={index}
          className="relative z-10 min-h-screen flex flex-col items-center justify-center text-center px-6 snap-start"
        >
          <motion.div
            initial={{ opacity: 0, y: 100, scale: 0.8 }}
            whileInView={{ opacity: 1, y: 0, scale: 1 }}
            transition={{ duration: 1.4 }}
            className="bg-white/70 backdrop-blur-xl p-10 rounded-[40px] shadow-2xl border border-pink-200 max-w-4xl glowEffect"
          >
            <h1 className="text-6xl md:text-8xl font-black text-rose-600 mb-8 animate-pulse">
              {slide.title}
            </h1>

            <p className="text-2xl md:text-3xl text-gray-700 leading-relaxed font-medium">
              {slide.text}
            </p>
          <button
              onClick={() => {
                const nextSection = sectionRefs.current[index + 1];
                if (nextSection) {
                  nextSection.scrollIntoView({ behavior: "smooth" });
                }
              }}
              className="mt-10 px-8 py-4 bg-rose-500 hover:bg-rose-600 text-white text-xl font-bold rounded-full shadow-xl transition-all duration-300 hover:scale-110"
            >
              Next Slide ➜
            </button>
          </motion.div>
        </section>
      ))}

      {/* Birthday Song Slide */}
      <section
        ref={(el) => {
            sectionRefs.current[slides.length] = el;
          }}
        className="relative z-10 min-h-screen flex items-center justify-center px-6 text-center"
      >
        <motion.div
          initial={{ opacity: 0, scale: 0.7 }}
          whileInView={{ opacity: 1, scale: 1 }}
          transition={{ duration: 1.3 }}
          className="bg-white/80 backdrop-blur-xl rounded-[40px] p-12 shadow-2xl border border-pink-200 max-w-4xl"
        >
          <h2 className="text-6xl font-black text-rose-600 mb-8">
            Birthday Song 🎵
          </h2>

          <p className="text-2xl text-gray-700 mb-8 leading-relaxed">
            Close your eyes and enjoy this special moment ✨
          </p>

          <audio controls autoPlay loop className="w-full rounded-2xl shadow-lg">
            <source
              src="https://cdn.pixabay.com/download/audio/2022/03/15/audio_c8c8a73467.mp3?filename=happy-birthday-to-you-piano-version-13976.mp3"
              type="audio/mp3"
            />
          </audio>

          <button
            onClick={() => {
              const nextSection = document.getElementById("surprise-section");
              if (nextSection) {
                nextSection.scrollIntoView({ behavior: "smooth" });
              }
            }}
            className="mt-10 px-8 py-4 bg-rose-500 hover:bg-rose-600 text-white text-xl font-bold rounded-full shadow-xl transition-all duration-300 hover:scale-110"
          >
            Next Slide ➜
          </button>
        </motion.div>
      </section>

      {/* Special Surprise Section */}
      <section
        ref={(el) => {
            sectionRefs.current[slides.length + 1] = el;
          }}
        id="surprise-section"
        className="relative z-10 min-h-screen flex flex-col justify-center py-20 px-6"
      >
        <h2 className="text-5xl font-bold text-center text-rose-600 mb-14 animate-pulse">
          Little Things About My Friend 🌸
        </h2>

        <div className="grid grid-cols-1 md:grid-cols-2 gap-8 max-w-5xl mx-auto">
          {surpriseQuotes.map((quote, index) => (
            <div
              key={index}
              className="bg-gradient-to-r from-pink-400 via-rose-300 to-pink-200 text-white rounded-3xl p-8 shadow-2xl hover:scale-105 transition-all duration-500"
            >
              <p className="text-2xl font-semibold leading-relaxed">
                {quote}
              </p>
            </div>
          ))}
        </div>

        <div className="mt-16 max-w-4xl mx-auto bg-white/80 backdrop-blur-lg rounded-3xl shadow-2xl p-10 border border-pink-200 text-center">
          <h3 className="text-4xl font-bold text-rose-500 mb-6">
            Best Friend Forever ⏳🤝
          </h3>
          <p className="text-xl text-gray-700 leading-relaxed">
            Your friendship means a lot to me and every memory with you is truly special. Thank you for always being supportive, funny, and amazing.
          </p>
        </div>

        <div className="text-center mt-14">
          <button
            onClick={() => {
              const nextSection = sectionRefs.current[slides.length + 2];
              if (nextSection) {
                nextSection.scrollIntoView({ behavior: "smooth" });
              }
            }}
            className="px-8 py-4 bg-rose-500 hover:bg-rose-600 text-white text-xl font-bold rounded-full shadow-xl transition-all duration-300 hover:scale-110"
          >
            Next Slide ➜
          </button>
        </div>
      </section>

      {/* Memories Section */}
      <section
        ref={(el) => {
            sectionRefs.current[slides.length + 2] = el;
          }}
        className="relative z-10 min-h-screen flex flex-col justify-center py-20 px-6"
      >
        <h2 className="text-5xl font-bold text-center text-rose-600 mb-16">
          Our Beautiful Memories 📸
        </h2>

        <div className="grid grid-cols-1 md:grid-cols-2 gap-10 max-w-6xl mx-auto">
          {memories.map((memory, index) => (
            <div
              key={index}
              className="bg-white/80 backdrop-blur-lg rounded-3xl shadow-2xl p-8 hover:scale-105 transition-transform duration-500 border border-pink-100"
            >
              <div className="text-6xl mb-4">{memory.emoji}</div>
              <h3 className="text-3xl font-bold text-rose-500 mb-4">
                {memory.title}
              </h3>
              <p className="text-lg text-gray-700 leading-relaxed">
                {memory.text}
              </p>
            </div>
          ))}
        </div>

        <div className="text-center mt-14">
          <button
            onClick={() => {
              const nextSection = sectionRefs.current[slides.length + 3];
              if (nextSection) {
                nextSection.scrollIntoView({ behavior: "smooth" });
              }
            }}
            className="px-8 py-4 bg-rose-500 hover:bg-rose-600 text-white text-xl font-bold rounded-full shadow-xl transition-all duration-300 hover:scale-110"
          >
            Next Slide ➜
          </button>
        </div>
      </section>

      {/* Photo Gallery Placeholder */}
      <section
        ref={(el) => {
            sectionRefs.current[slides.length + 3] = el;
          }}
        className="relative z-10 min-h-screen flex flex-col justify-center py-20 px-6 bg-white/40 backdrop-blur-md"
      >
        <h2 className="text-5xl font-bold text-center text-rose-600 mb-16">
          Gallery of Memories 🌸
        </h2>

        <div className="grid grid-cols-1 sm:grid-cols-2 md:grid-cols-3 gap-8 max-w-6xl mx-auto">
          {[1, 2, 3, 4, 5, 6].map((item) => (
            <div
              key={item}
              className="h-64 rounded-3xl bg-gradient-to-br from-pink-300 to-rose-200 shadow-2xl flex items-center justify-center text-2xl font-bold text-white hover:rotate-2 hover:scale-105 transition-all duration-500"
            >
              Add Your Photo {item}
            </div>
          ))}
        </div>
      </section>

      {/* Friendship Promise Section */}
      <section className="relative z-10 min-h-screen flex flex-col justify-center px-6 py-20 bg-gradient-to-b from-rose-100 to-pink-200">
        <h2 className="text-6xl font-black text-center text-rose-600 mb-16">
          Friendship Promises 🤝
        </h2>

        <div className="max-w-5xl mx-auto grid grid-cols-1 md:grid-cols-2 gap-8">
          {friendshipPromises.map((promise, index) => (
            <motion.div
              key={index}
              initial={{ opacity: 0, y: 60 }}
              whileInView={{ opacity: 1, y: 0 }}
              transition={{ duration: 1 }}
              className="bg-white/80 p-8 rounded-3xl shadow-2xl border border-pink-200"
            >
              <p className="text-2xl font-bold text-rose-500 leading-relaxed">
                {promise}
              </p>
            </motion.div>
          ))}
        </div>
      </section>

      {/* Timeline Section */}
      <section className="relative z-10 min-h-screen flex flex-col justify-center px-6 py-20">
        <h2 className="text-6xl font-black text-center text-rose-600 mb-20">
          Our Friendship Timeline ⏳
        </h2>

        <div className="max-w-4xl mx-auto space-y-10">
          {timelineMoments.map((moment, index) => (
            <motion.div
              key={index}
              initial={{ opacity: 0, x: -100 }}
              whileInView={{ opacity: 1, x: 0 }}
              transition={{ duration: 1 }}
              className="bg-white/80 rounded-3xl p-10 shadow-2xl border-l-[12px] border-rose-400"
            >
              <h3 className="text-4xl font-black text-rose-500 mb-4">
                {moment.year}
              </h3>
              <p className="text-2xl text-gray-700 leading-relaxed">
                {moment.desc}
              </p>
            </motion.div>
          ))}
        </div>
      </section>

      {/* Cake Wishes Section */}
      <section className="relative z-10 min-h-screen flex flex-col justify-center px-6 py-24 bg-gradient-to-b from-pink-100 to-rose-200">
        <h2 className="text-6xl font-black text-center text-rose-600 mb-16">
          Sweet Birthday Wishes 🎂
        </h2>

        <div className="grid grid-cols-1 md:grid-cols-2 gap-10 max-w-6xl mx-auto">
          {cakeMessages.map((message, index) => (
            <motion.div
              key={index}
              initial={{ opacity: 0, rotate: -5, scale: 0.8 }}
              whileInView={{ opacity: 1, rotate: 0, scale: 1 }}
              transition={{ duration: 1 }}
              className="bg-white/80 rounded-[35px] p-10 shadow-2xl border border-pink-200"
            >
              <div className="text-7xl mb-6">🎂</div>
              <p className="text-2xl text-gray-700 font-semibold leading-relaxed">
                {message}
              </p>
            </motion.div>
          ))}
        </div>
      </section>

      {/* Fun Facts Section */}
      <section className="relative z-10 min-h-screen flex flex-col justify-center px-6 py-24">
        <h2 className="text-6xl font-black text-center text-rose-600 mb-20">
          Fun Facts About You 😂
        </h2>

        <div className="max-w-5xl mx-auto space-y-10">
          {funFacts.map((fact, index) => (
            <motion.div
              key={index}
              initial={{ opacity: 0, x: index % 2 === 0 ? -120 : 120 }}
              whileInView={{ opacity: 1, x: 0 }}
              transition={{ duration: 1 }}
              className="bg-white/80 rounded-[35px] p-10 shadow-2xl border border-pink-200 text-center"
            >
              <p className="text-3xl font-black text-rose-500 leading-relaxed">
                {fact}
              </p>
            </motion.div>
          ))}
        </div>
      </section>

      {/* Letter Section */}
      <section className="relative z-10 min-h-screen flex flex-col justify-center px-6 py-24 bg-gradient-to-b from-rose-100 to-pink-100">
        <motion.div
          initial={{ opacity: 0, y: 100 }}
          whileInView={{ opacity: 1, y: 0 }}
          transition={{ duration: 1.2 }}
          className="max-w-5xl mx-auto bg-white/80 rounded-[45px] p-12 shadow-2xl border border-pink-200"
        >
          <h2 className="text-6xl font-black text-center text-rose-600 mb-12">
            A Letter For You 💌
          </h2>

          <div className="space-y-8">
            {letterParagraphs.map((para, index) => (
              <p
                key={index}
                className="text-2xl text-gray-700 leading-[2.2rem] font-medium"
              >
                {para}
              </p>
            ))}
          </div>
        </motion.div>
      </section>

      {/* Star Message Section */}
      <section className="relative z-10 min-h-screen flex flex-col justify-center px-6 py-24 bg-gradient-to-b from-purple-100 to-pink-100">
        <h2 className="text-6xl font-black text-center text-rose-600 mb-20">
          Messages From The Stars ✨
        </h2>

        <div className="max-w-6xl mx-auto grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-10">
          {starMessages.map((msg, index) => (
            <motion.div
              key={index}
              initial={{ opacity: 0, y: 80 }}
              whileInView={{ opacity: 1, y: 0 }}
              transition={{ duration: 1 }}
              className="bg-white/80 rounded-[35px] p-10 shadow-2xl border border-pink-200 text-center"
            >
              <div className="text-6xl mb-6">🌟</div>
              <p className="text-2xl font-bold text-rose-500 leading-relaxed">
                {msg}
              </p>
            </motion.div>
          ))}
        </div>
      </section>

      {/* Why You Are Special */}
      <section className="relative z-10 min-h-screen flex flex-col justify-center px-6 py-24">
        <h2 className="text-6xl font-black text-center text-rose-600 mb-20">
          Why You Are Special 💕
        </h2>

        <div className="max-w-5xl mx-auto space-y-10">
          {birthdayReasons.map((reason, index) => (
            <motion.div
              key={index}
              initial={{ opacity: 0, scale: 0.8 }}
              whileInView={{ opacity: 1, scale: 1 }}
              transition={{ duration: 1 }}
              className="bg-gradient-to-r from-pink-300 via-rose-200 to-pink-100 rounded-[40px] p-10 shadow-2xl text-center"
            >
              <p className="text-3xl font-black text-rose-700 leading-relaxed">
                {reason}
              </p>
            </motion.div>
          ))}
        </div>
      </section>

      {/* Final Message */}
      <footer className="relative z-10 py-20 text-center px-6 arrivalAnimation">
        <h2 className="text-5xl font-extrabold text-rose-600 animate-pulse">
          Lucky To Have A Friend Like You 🤝
        </h2>
        <p className="mt-6 text-xl text-gray-700 max-w-3xl mx-auto leading-relaxed">
          No matter how many birthdays pass, I’ll always cherish every memory we
          create together. Thank you for being the most wonderful part of my
          life. Happy Birthday once again! 🎂✨
        </p>
      </footer>
    </div>
  );
}
