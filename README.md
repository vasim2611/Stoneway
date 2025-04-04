/* STONEWAY – Metaverse Fashion Emporium + Red Carpet Styling Residency */ import React, { useState } from "react"; import { Button } from "@/components/ui/button"; import { Card, CardContent } from "@/components/ui/card"; import { Input } from "@/components/ui/input"; import { Globe2, Sparkles } from "lucide-react";

export default function StonewayHome() { const [showMetaverse, setShowMetaverse] = useState(false); const [showResidency, setShowResidency] = useState(false);

return ( <div className="min-h-screen bg-white text-black"> {/* Metaverse Fashion Emporium */} <section className="py-20 px-6 bg-gradient-to-br from-[#fcf4ff] to-[#f5eaff] text-center"> <Globe2 className="mx-auto w-10 h-10 text-purple-800" /> <h2 className="text-4xl font-bold mt-3 mb-2">Metaverse Fashion Emporium</h2> <p className="text-gray-700 max-w-xl mx-auto mb-6">Step into our digital flagship where you can explore, try-on, and purchase Stoneway’s digital couture for your avatar—and claim real-world exclusives along the way.</p> <Button className="bg-purple-800 text-white px-6 py-2 rounded-full text-lg" onClick={() => setShowMetaverse(true)}> Enter Virtual Store </Button> </section>

{showMetaverse && (
    <div className="fixed inset-0 bg-black bg-opacity-85 z-50 flex items-center justify-center">
      <div className="bg-white p-6 rounded-2xl shadow-2xl max-w-xl w-full text-center">
        <h3 className="text-2xl font-bold mb-4">Join the Metaverse Experience</h3>
        <p className="text-gray-600 mb-4">Your digital wardrobe awaits. Secure your fashion-forward identity.</p>
        <Input placeholder="Name / Handle" className="mb-3" />
        <Input placeholder="Wallet Address or Email" className="mb-4" />
        <Button className="bg-black text-white w-full">Join Now</Button>
        <Button variant="ghost" className="mt-4" onClick={() => setShowMetaverse(false)}>Close</Button>
      </div>
    </div>
  )}

  {/* Red Carpet Styling Residency */}
  <section className="py-20 px-6 bg-gradient-to-br from-[#fff9f2] to-[#fceee4] text-center">
    <Sparkles className="mx-auto w-10 h-10 text-rose-800" />
    <h2 className="text-4xl font-bold mt-3 mb-2">Red Carpet Styling Residency</h2>
    <p className="text-gray-700 max-w-xl mx-auto mb-6">Live the red carpet fantasy. A week-long residency with elite stylists, personal designers, fittings, and appearances culminating in your grand entrance at a global fashion gala.</p>
    <Button className="bg-rose-800 text-white px-6 py-2 rounded-full text-lg" onClick={() => setShowResidency(true)}>
      Apply for Residency
    </Button>
  </section>

  {showResidency && (
    <div className="fixed inset-0 bg-black bg-opacity-80 z-50 flex items-center justify-center">
      <div className="bg-white p-6 rounded-2xl shadow-2xl max-w-xl w-full text-center">
        <h3 className="text-2xl font-bold mb-4">Styling Residency Application</h3>
        <p className="text-gray-600 mb-4">This experience is curated for a global few. Share your details to be considered for our next red carpet transformation.</p>
        <Input placeholder="Full Name" className="mb-3" />
        <Input placeholder="Email Address" className="mb-3" />
        <Input placeholder="Style Portfolio or Instagram" className="mb-4" />
        <Button className="bg-black text-white w-full">Submit Application</Button>
        <Button variant="ghost" className="mt-4" onClick={() => setShowResidency(false)}>Close</Button>
      </div>
    </div>
  )}
</div>

); }

