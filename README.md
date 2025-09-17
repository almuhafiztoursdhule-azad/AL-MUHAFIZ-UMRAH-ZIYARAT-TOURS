# AL-MUHAFIZ-UMRAH-ZIYARAT-TOURS
AL MUHAFIZ UMRAH ZIYARAT TOURS
import React, { useState } from "react";

export default function App() {
  const [lang, setLang] = useState("en");

  const text = {
    en: {
      title: "AL Muhafiz Umrah Ziyarat Tours",
      home: "Home",
      packages: "Packages",
      services: "Services & More",
      booking: "Booking",
      discounts: "Advance & Discounts",
      gallery: "Photo & Video Gallery",
      contact: "Contact Us",
      switch: "اردو",
      welcome: "Welcome to AL Muhafiz Umrah Ziyarat Tours",
      intro:
        "We provide the best Umrah & Ziyarat packages with full comfort, guidance and trust.",
      whatsapp: "Book on WhatsApp",
    },
    ur: {
      title: "المحافظ عمرہ زیارت ٹورز",
      home: "ہوم",
      packages: "پیکجز",
      services: "سروسز اور مزید",
      booking: "بکنگ",
      discounts: "ایڈوانس اور ڈسکاونٹس",
      gallery: "فوٹو اور ویڈیو گیلری",
      contact: "رابطہ کریں",
      switch: "English",
      welcome: "المحافظ عمرہ زیارت ٹورز میں خوش آمدید",
      intro:
        "ہم بہترین عمرہ اور زیارت پیکجز فراہم کرتے ہیں، مکمل سہولت، رہنمائی اور اعتماد کے ساتھ۔",
      whatsapp: "واٹس ایپ پر بک کریں",
    },
  };

  const t = text[lang];

  return (
    <div className="font-sans bg-gray-100 min-h-screen">
      {/* Header */}
      <header className="bg-blue-900 text-white p-4 flex justify-between items-center">
        <h1 className="text-xl font-bold">{t.title}</h1>
        <nav className="space-x-4">
          <button onClick={() => setLang(lang === "en" ? "ur" : "en")} className="bg-yellow-400 px-2 py-1 rounded">
            {t.switch}
          </button>
        </nav>
      </header>

      {/* Navigation */}
      <nav className="bg-gray-200 p-3 flex justify-center space-x-4 text-sm md:text-base">
        <a href="#home" className="hover:text-blue-700">{t.home}</a>
        <a href="#packages" className="hover:text-blue-700">{t.packages}</a>
        <a href="#services" className="hover:text-blue-700">{t.services}</a>
        <a href="#booking" className="hover:text-blue-700">{t.booking}</a>
        <a href="#discounts" className="hover:text-blue-700">{t.discounts}</a>
        <a href="#gallery" className="hover:text-blue-700">{t.gallery}</a>
        <a href="#contact" className="hover:text-blue-700">{t.contact}</a>
      </nav>

      {/* Sections */}
      <section id="home" className="p-10 text-center">
        <h2 className="text-2xl font-bold mb-4">{t.welcome}</h2>
        <p className="max-w-2xl mx-auto">{t.intro}</p>
      </section>

      <section id="packages" className="p-10 bg-white shadow-md rounded-lg m-5">
        <h2 className="text-xl font-bold mb-3">{t.packages}</h2>
        <ul className="list-disc pl-5">
          <li>Economy Package – 7 Days</li>
          <li>Standard Package – 15 Days</li>
          <li>VIP Package – 21 Days</li>
        </ul>
      </section>

      <section id="services" className="p-10 bg-white shadow-md rounded-lg m-5">
        <h2 className="text-xl font-bold mb-3">{t.services}</h2>
        <ul className="list-disc pl-5">
          <li>Flight Booking</li>
          <li>Hotel Accommodation</li>
          <li>Guided Ziyarat Tours</li>
          <li>24/7 Customer Support</li>
        </ul>
      </section>

      <section id="booking" className="p-10 bg-white shadow-md rounded-lg m-5">
        <h2 className="text-xl font-bold mb-3">{t.booking}</h2>
        <p>Fill the booking form and get connected directly on WhatsApp.</p>
        <a
          href="https://wa.me/919273913286"
          target="_blank"
          rel="noopener noreferrer"
          className="bg-green-600 text-white px-4 py-2 rounded mt-3 inline-block"
        >
          {t.whatsapp}
        </a>
      </section>

      <section id="discounts" className="p-10 bg-white shadow-md rounded-lg m-5">
        <h2 className="text-xl font-bold mb-3">{t.discounts}</h2>
        <p>Book early and avail special discounts on selected packages!</p>
      </section>

      <section id="gallery" className="p-10 bg-white shadow-md rounded-lg m-5">
        <h2 className="text-xl font-bold mb-3">{t.gallery}</h2>
        <div className="grid grid-cols-2 md:grid-cols-3 gap-4">
          <img src="https://via.placeholder.com/200" alt="Gallery 1" className="rounded-lg shadow" />
          <img src="https://via.placeholder.com/200" alt="Gallery 2" className="rounded-lg shadow" />
          <img src="https://via.placeholder.com/200" alt="Gallery 3" className="rounded-lg shadow" />
        </div>
      </section>

      <section id="contact" className="p-10 bg-white shadow-md rounded-lg m-5">
        <h2 className="text-xl font-bold mb-3">{t.contact}</h2>
        <form
          action={`https://wa.me/919273913286`}
          method="get"
          target="_blank"
          className="space-y-3"
        >
          <input
            type="text"
            name="name"
            placeholder="Your Name"
            className="w-full p-2 border rounded"
          />
          <input
            type="text"
            name="details"
            placeholder="Package Details"
            className="w-full p-2 border rounded"
          />
          <button type="submit" className="bg-blue-600 text-white px-4 py-2 rounded">
            {t.whatsapp}
          </button>
        </form>
      </section>

      {/* Footer */}
      <footer className="bg-blue-900 text-white text-center p-4 mt-10">
        © 2025 {t.title} | All Rights Reserved
      </footer>
    </div>
  );
}
