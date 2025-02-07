import React from "react";
import { FaFacebook, FaTwitter, FaInstagram } from "react-icons/fa";
import Image from "next/image";

export default function CEIWebsite() {
  return (
    <div className="bg-yellow-100 min-h-screen text-gray-900">
      {/* Navbar */}
      <nav className="bg-yellow-700 text-white p-4 flex justify-between items-center">
        <h1 className="text-2xl font-bold">CEI</h1>
        <ul className="flex space-x-4">
          <li><a href="#about" className="hover:underline">About</a></li>
          <li><a href="#programs" className="hover:underline">Programs</a></li>
          <li><a href="#gallery" className="hover:underline">Gallery</a></li>
          <li><a href="#events" className="hover:underline">Events</a></li>
          <li><a href="#blog" className="hover:underline">Blog</a></li>
          <li><a href="#support" className="hover:underline">Support Us</a></li>
          <li><a href="#contact" className="hover:underline">Contact</a></li>
        </ul>
      </nav>
      {/* Hero Section with Background Image */}
      <header className="relative h-[60vh] flex items-center justify-center overflow-hidden bg-cover bg-center" style={{ backgroundImage: "url('/cei-intro.jpg')" }}>
        <div className="absolute inset-0 bg-black bg-opacity-50 flex justify-center items-center">
          <div className="relative w-[200px] h-[200px]">
            <Image src="/cei-logo.png" layout="fill" objectFit="contain" alt="CEI Logo" />
          </div>
        </div>
      </header>
      {/* Gallery */}
      <section id="gallery" className="p-8">
        <h3 className="text-3xl font-bold text-yellow-700">Gallery</h3>
        <div className="grid grid-cols-2 md:grid-cols-4 gap-4 mt-4">
          <Image src="/gallery1.jpg" width={300} height={200} className="rounded-lg" alt="Cultural Event" />
          <Image src="/gallery2.jpg" width={300} height={200} className="rounded-lg" alt="Traditional Crafts" />
          <Image src="/gallery3.jpg" width={300} height={200} className="rounded-lg" alt="Community Workshops" />
          <Image src="/gallery4.jpg" width={300} height={200} className="rounded-lg" alt="African Dance Performance" />
        </div>
      </section>
      {/* Footer */}
      <footer className="bg-yellow-700 text-white p-4 text-center">
        <p>&copy; {new Date().getFullYear()} CEI. All Rights Reserved.</p>
        <div className="flex justify-center space-x-4 mt-2">
          <FaFacebook className="cursor-pointer" />
          <FaTwitter className="cursor-pointer" />
          <FaInstagram className="cursor-pointer" />
        </div>
      </footer>
    </div>
