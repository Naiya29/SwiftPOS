# SwiftPOS
import React from "react";
import { CheckCircle, Store, Gift, BarChart, Mail, DollarSign, TrendingUp, Calendar, Smartphone, Shield, Users, Cloud } from "lucide-react";
import { LineChart, Line, CartesianGrid, XAxis, YAxis, Tooltip, ResponsiveContainer } from "recharts";

const monthlyData = [
  { month: "Jan", revenue: 4000, expenses: 2400 },
  { month: "Feb", revenue: 5000, expenses: 2600 },
  { month: "Mar", revenue: 6000, expenses: 3000 },
  { month: "Apr", revenue: 7000, expenses: 3200 },
  { month: "May", revenue: 8000, expenses: 3500 },
];

export default function Home() {
  return (
    <main className="min-h-screen bg-white text-gray-800 px-6 py-12">
      {/* Hero Section */}
      <section className="max-w-7xl mx-auto text-center mb-20">
        <h1 className="text-5xl font-bold mb-4">SwiftPOS</h1>
        <p className="text-lg mb-6">
          Cloud-Based POS with Real-Time Inventory and Loyalty Management for Small Businesses
        </p>
        <a href="#contact" className="inline-block bg-indigo-600 text-white text-lg px-6 py-3 rounded-xl hover:bg-indigo-700 transition">Request Demo</a>
      </section>

      {/* Features Section */}
      <section className="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-4 gap-8 max-w-6xl mx-auto mb-20">
        {[{
          Icon: Store,
          title: "Smart POS",
          description: "Fast, simple billing interface with digital receipts and offline sync."
        }, {
          Icon: CheckCircle,
          title: "Inventory Tracking",
          description: "Real-time stock management with low-stock alerts and analytics."
        }, {
          Icon: Gift,
          title: "Loyalty Program",
          description: "Reward customers with points, discounts, and special offers automatically."
        }, {
          Icon: BarChart,
          title: "Analytics",
          description: "Visualize sales performance and customer behavior with ease."
        }, {
          Icon: Smartphone,
          title: "Mobile Access",
          description: "Monitor and manage your store remotely from any device."
        }, {
          Icon: Shield,
          title: "Secure Payments",
          description: "End-to-end encrypted transactions for secure customer experiences."
        }, {
          Icon: Users,
          title: "Multi-User Roles",
          description: "Assign roles and permissions to staff for better control."
        }, {
          Icon: Cloud,
          title: "Cloud Backup",
          description: "Automatic backups keep your data safe and accessible."
        }].map(({ Icon, title, description }, index) => (
          <div key={index} className="shadow-xl rounded-2xl bg-white p-6 text-center">
            <Icon className="mx-auto h-12 w-12 text-indigo-600 mb-4" />
            <h3 className="text-xl font-semibold mb-2">{title}</h3>
            <p>{description}</p>
          </div>
        ))}
      </section>

      {/* Financial Dashboard Section */}
      <section id="dashboard" className="bg-gray-50 py-16 px-4">
        <div className="max-w-6xl mx-auto">
          <h2 className="text-3xl font-bold mb-10 text-center">Finance Dashboard</h2>
          <div className="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-4 gap-6 mb-12">
            <div className="bg-white rounded-2xl p-6 shadow flex flex-col items-center text-center">
              <DollarSign className="h-8 w-8 text-green-500 mb-2" />
              <h3 className="text-xl font-bold">Total Revenue</h3>
              <p className="text-2xl text-green-600 font-semibold mt-2">$23,400</p>
            </div>
            <div className="bg-white rounded-2xl p-6 shadow flex flex-col items-center text-center">
              <TrendingUp className="h-8 w-8 text-blue-500 mb-2" />
              <h3 className="text-xl font-bold">Expenses</h3>
              <p className="text-2xl text-red-500 font-semibold mt-2">$7,820</p>
            </div>
            <div className="bg-white rounded-2xl p-6 shadow flex flex-col items-center text-center">
              <BarChart className="h-8 w-8 text-purple-500 mb-2" />
              <h3 className="text-xl font-bold">Profit</h3>
              <p className="text-2xl text-purple-600 font-semibold mt-2">$15,580</p>
            </div>
            <div className="bg-white rounded-2xl p-6 shadow flex flex-col items-center text-center">
              <Calendar className="h-8 w-8 text-yellow-500 mb-2" />
              <h3 className="text-xl font-bold">Monthly Summary</h3>
              <p className="text-md mt-2 text-gray-700">Revenue and expenses by month</p>
            </div>
          </div>

          {/* Finance Chart */}
          <div className="bg-white rounded-2xl shadow p-6">
            <h3 className="text-xl font-semibold mb-4">Monthly Revenue vs Expenses</h3>
            <ResponsiveContainer width="100%" height={300}>
              <LineChart data={monthlyData} margin={{ top: 10, right: 20, left: 0, bottom: 0 }}>
                <Line type="monotone" dataKey="revenue" stroke="#4F46E5" strokeWidth={3} />
                <Line type="monotone" dataKey="expenses" stroke="#EF4444" strokeWidth={3} />
                <CartesianGrid stroke="#ccc" strokeDasharray="5 5" />
                <XAxis dataKey="month" />
                <YAxis />
                <Tooltip />
              </LineChart>
            </ResponsiveContainer>
          </div>
        </div>
      </section>

      {/* Call to Action */}
      <section className="text-center max-w-2xl mx-auto mb-20">
        <h2 className="text-3xl font-bold mb-4">Grow Your Business with SwiftPOS</h2>
        <p className="text-lg mb-6">
          Join hundreds of small businesses upgrading their operations with our powerful yet affordable POS solution.
        </p>
        <a href="#contact" className="inline-block bg-indigo-600 text-white text-lg px-6 py-3 rounded-xl hover:bg-indigo-700 transition">Get Started</a>
      </section>

      {/* Contact Section */}
      <section id="contact" className="bg-gray-100 py-16 px-4">
        <div className="max-w-xl mx-auto text-center">
          <h2 className="text-3xl font-bold mb-6">Contact Us</h2>
          <form className="space-y-6">
            <input type="text" placeholder="Your Name" className="w-full px-4 py-3 rounded-lg border border-gray-300 focus:outline-none focus:ring-2 focus:ring-indigo-500" />
            <input type="email" placeholder="Your Email" className="w-full px-4 py-3 rounded-lg border border-gray-300 focus:outline-none focus:ring-2 focus:ring-indigo-500" />
            <textarea placeholder="Your Message" rows="4" className="w-full px-4 py-3 rounded-lg border border-gray-300 focus:outline-none focus:ring-2 focus:ring-indigo-500"></textarea>
            <button type="submit" className="bg-indigo-600 text-white px-6 py-3 rounded-xl hover:bg-indigo-700 transition flex items-center justify-center gap-2">
              <Mail className="w-5 h-5" /> Send Message
            </button>
          </form>
        </div>
      </section>

      {/* Footer */}
      <footer className="text-center py-8 border-t text-sm text-gray-600">
        © {new Date().getFullYear()} SwiftPOS. All rights reserved.
      </footer>
    </main>
  );
}
