import React, { useState, useEffect } from "react";
import { Card, CardContent } from "@/components/ui/card";
import { Button } from "@/components/ui/button";
import { Tabs, TabsContent, TabsList, TabsTrigger } from "@/components/ui/tabs";

export default function NordiCityRP() {
  const [darkMode, setDarkMode] = useState(false);

  useEffect(() => {
    document.body.className = darkMode ? "bg-gray-900 text-white" : "bg-orange-100 text-gray-800";
  }, [darkMode]);

  return (
    <div className="min-h-screen p-6 space-y-12 transition-colors">
      {/* Header */}
      <header className="flex items-center justify-between">
        <div className="flex items-center space-x-4">
          <img src="/Nordi.png" alt="Nordi Logo" className="h-14" />
          <h1 className="text-3xl font-bold">Nordi-City RP</h1>
        </div>
        <div className="space-x-4">
          <Button variant="outline" onClick={() => window.open("https://nordi-city.tebex.io", "_blank")}>Shop</Button>
          <Button variant="default" onClick={() => window.open("https://discord.gg/nordi", "_blank")}>Discord</Button>
          <Button onClick={() => setDarkMode(!darkMode)}>
            {darkMode ? "☀️ Light Mode" : "🌙 Dark Mode"}
          </Button>
        </div>
      </header>

      {/* Live Ticker */}
      <section className="bg-white/70 dark:bg-gray-800 rounded-2xl shadow p-4 text-center text-sm">
        <p>📢 <strong>Live-Ticker:</strong> Server online! Nächster Event: Drift Night am Samstag 20 Uhr!</p>
      </section>

      {/* Regelwerk */}
      <section className="space-y-6">
        <h2 className="text-2xl font-semibold">📜 Regelwerke</h2>
        <Tabs defaultValue="allgemein" className="w-full">
          <TabsList className="grid grid-cols-2 w-full">
            <TabsTrigger value="allgemein">Allgemeines Regelwerk</TabsTrigger>
            <TabsTrigger value="illegal">Illegales Regelwerk</TabsTrigger>
          </TabsList>

          <TabsContent value="allgemein">
            <Card className="bg-white/80 dark:bg-gray-800 p-4 max-h-[600px] overflow-y-auto">
              <CardContent className="prose prose-sm max-w-none">
                <iframe
                  src="/Offizielles-Regelwerk.pdf"
                  title="Allgemeines Regelwerk"
                  width="100%"
                  height="800px"
                  className="w-full h-[800px] border-none rounded-xl"
                ></iframe>
              </CardContent>
            </Card>
          </TabsContent>

          <TabsContent value="illegal">
            <Card className="bg-white/80 dark:bg-gray-800 p-4 max-h-[600px] overflow-y-auto">
              <CardContent className="prose prose-sm max-w-none">
                <iframe
                  src="/Illegales-Fraktions-Regelwerk.pdf"
                  title="Illegales Regelwerk"
                  width="100%"
                  height="800px"
                  className="w-full h-[800px] border-none rounded-xl"
                ></iframe>
              </CardContent>
            </Card>
          </TabsContent>
        </Tabs>
      </section>

      {/* Tebex Shop eingebettet */}
      <section className="space-y-6">
        <h2 className="text-2xl font-semibold">🛒 Nordi-City Shop</h2>
        <div className="aspect-video rounded-xl overflow-hidden shadow-lg border border-gray-300 dark:border-gray-700">
          <iframe
            src="https://nordi-city.tebex.io"
            title="Tebex Shop"
            width="100%"
            height="100%"
            frameBorder="0"
            className="w-full h-[600px]"
          ></iframe>
        </div>
      </section>

      {/* Footer */}
      <footer className="text-center text-xs text-gray-500 dark:text-gray-400">
        &copy; {new Date().getFullYear()} Nordi-City RP – Alle Rechte vorbehalten.
      </footer>
    </div>
  );
}
import React, { useState, useEffect } from "react";
import { Card, CardContent } from "@/components/ui/card";
import { Button } from "@/components/ui/button";
import { Tabs, TabsContent, TabsList, TabsTrigger } from "@/components/ui/tabs";

export default function NordiCityRP() {
  const [darkMode, setDarkMode] = useState(false);

  useEffect(() => {
    document.body.className = darkMode ? "bg-gray-900 text-white" : "bg-orange-100 text-gray-800";
  }, [darkMode]);

  return (
    <div className="min-h-screen p-6 space-y-12 transition-colors">
      {/* Header */}
      <header className="flex items-center justify-between">
        <div className="flex items-center space-x-4">
          <img src="/Nordi.png" alt="Nordi Logo" className="h-14" />
          <h1 className="text-3xl font-bold">Nordi-City RP</h1>
        </div>
        <div className="space-x-4">
          <Button variant="outline" onClick={() => window.open("https://nordi-city.tebex.io", "_blank")}>Shop</Button>
          <Button variant="default" onClick={() => window.open("https://discord.gg/nordi", "_blank")}>Discord</Button>
          <Button onClick={() => setDarkMode(!darkMode)}>
            {darkMode ? "☀️ Light Mode" : "🌙 Dark Mode"}
          </Button>
        </div>
      </header>

      {/* Live Ticker */}
      <section className="bg-white/70 dark:bg-gray-800 rounded-2xl shadow p-4 text-center text-sm">
        <p>📢 <strong>Live-Ticker:</strong> Server online! Nächster Event: Drift Night am Samstag 20 Uhr!</p>
      </section>

      {/* Regelwerk */}
      <section className="space-y-6">
        <h2 className="text-2xl font-semibold">📜 Regelwerke</h2>
        <Tabs defaultValue="allgemein" className="w-full">
          <TabsList className="grid grid-cols-2 w-full">
            <TabsTrigger value="allgemein">Allgemeines Regelwerk</TabsTrigger>
            <TabsTrigger value="illegal">Illegales Regelwerk</TabsTrigger>
          </TabsList>

          <TabsContent value="allgemein">
            <Card className="bg-white/80 dark:bg-gray-800 p-4 max-h-[600px] overflow-y-auto">
              <CardContent className="prose prose-sm max-w-none">
                <iframe
                  src="/Offizielles-Regelwerk.pdf"
                  title="Allgemeines Regelwerk"
                  width="100%"
                  height="800px"
                  className="w-full h-[800px] border-none rounded-xl"
                ></iframe>
              </CardContent>
            </Card>
          </TabsContent>

          <TabsContent value="illegal">
            <Card className="bg-white/80 dark:bg-gray-800 p-4 max-h-[600px] overflow-y-auto">
              <CardContent className="prose prose-sm max-w-none">
                <iframe
                  src="/Illegales-Fraktions-Regelwerk.pdf"
                  title="Illegales Regelwerk"
                  width="100%"
                  height="800px"
                  className="w-full h-[800px] border-none rounded-xl"
                ></iframe>
              </CardContent>
            </Card>
          </TabsContent>
        </Tabs>
      </section>

      {/* Tebex Shop eingebettet */}
      <section className="space-y-6">
        <h2 className="text-2xl font-semibold">🛒 Nordi-City Shop</h2>
        <div className="aspect-video rounded-xl overflow-hidden shadow-lg border border-gray-300 dark:border-gray-700">
          <iframe
            src="https://nordi-city.tebex.io"
            title="Tebex Shop"
            width="100%"
            height="100%"
            frameBorder="0"
            className="w-full h-[600px]"
          ></iframe>
        </div>
      </section>

      {/* Footer */}
      <footer className="text-center text-xs text-gray-500 dark:text-gray-400">
        &copy; {new Date().getFullYear()} Nordi-City RP – Alle Rechte vorbehalten.
      </footer>
    </div>
  );
}
