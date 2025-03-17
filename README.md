import React from "react";
import { BrowserRouter as Router, Route, Routes, Link } from "react-router-dom";
import { Card, CardContent } from "@/components/ui/card";
import { Button } from "@/components/ui/button";

const Home = () => (
  <div className="p-6 text-center">
    <h1 className="text-3xl font-bold">Lira Recruitment Agency</h1>
    <p className="mt-2 text-gray-600">আপনার স্বপ্নের চাকরি এখন আরও সহজ</p>
    <Link to="/jobs">
      <Button className="mt-4">চাকরি দেখুন</Button>
    </Link>
  </div>
);

const Jobs = () => (
  <div className="p-6">
    <h2 className="text-2xl font-bold">চাকরির সুযোগ</h2>
    <Card className="mt-4">
      <CardContent>
        <h3 className="text-xl font-semibold">কনস্ট্রাকশন ওয়ার্কার - সৌদি আরব</h3>
        <p>বেতন: 1500 SAR + অতিরিক্ত সুবিধা</p>
        <Button className="mt-2">আবেদন করুন</Button>
      </CardContent>
    </Card>
  </div>
);

const Contact = () => (
  <div className="p-6">
    <h2 className="text-2xl font-bold">যোগাযোগ করুন</h2>
    <p>Email: info@lirarecruitment.com</p>
    <p>Phone: +880 1234 567890</p>
  </div>
);

const App = () => {
  return (
    <Router>
      <nav className="p-4 bg-blue-600 text-white flex justify-between">
        <Link to="/" className="font-bold">Lira Recruitment</Link>
        <div>
          <Link to="/jobs" className="mr-4">চাকরির সুযোগ</Link>
          <Link to="/contact">যোগাযোগ</Link>
        </div>
      </nav>
      <Routes>
        <Route path="/" element={<Home />} />
        <Route path="/jobs" element={<Jobs />} />
        <Route path="/contact" element={<Contact />} />
      </Routes>
    </Router>
  );
};

export default App;
