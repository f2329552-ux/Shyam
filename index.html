🗂️ FRONTEND — artifacts/vidcoins/src/
main.tsx
import { createRoot } from "react-dom/client";
import App from "./App";
import "./index.css";
createRoot(document.getElementById("root")!).render(<App />);
index.css
@import "tailwindcss";
@import "tw-animate-css";
@plugin "@tailwindcss/typography";
@custom-variant dark (&:is(.dark *));
@theme inline {
  --color-background: hsl(var(--background));
  --color-foreground: hsl(var(--foreground));
  --color-border: hsl(var(--border));
  --color-input: hsl(var(--input));
  --color-ring: hsl(var(--ring));
  --color-card: hsl(var(--card));
  --color-card-foreground: hsl(var(--card-foreground));
  --color-popover: hsl(var(--popover));
  --color-popover-foreground: hsl(var(--popover-foreground));
  --color-primary: hsl(var(--primary));
  --color-primary-foreground: hsl(var(--primary-foreground));
  --color-secondary: hsl(var(--secondary));
  --color-secondary-foreground: hsl(var(--secondary-foreground));
  --color-muted: hsl(var(--muted));
  --color-muted-foreground: hsl(var(--muted-foreground));
  --color-accent: hsl(var(--accent));
  --color-accent-foreground: hsl(var(--accent-foreground));
  --color-destructive: hsl(var(--destructive));
  --color-destructive-foreground: hsl(var(--destructive-foreground));
  --font-sans: "Outfit", sans-serif;
  --radius-sm: calc(var(--radius) - 4px);
  --radius-md: calc(var(--radius) - 2px);
  --radius-lg: var(--radius);
  --radius-xl: calc(var(--radius) + 4px);
}
:root {
  --background: 40 33% 98%;
  --foreground: 220 10% 20%;
  --border: 40 20% 85%;
  --input: 40 20% 85%;
  --ring: 28 100% 60%;
  --card: 0 0% 100%;
  --card-foreground: 220 10% 20%;
  --popover: 0 0% 100%;
  --popover-foreground: 220 10% 20%;
  /* Saffron */
  --primary: 28 100% 60%;
  --primary-foreground: 0 0% 100%;
  /* Deep Green */
  --secondary: 115 89% 28%;
  --secondary-foreground: 0 0% 100%;
  --muted: 40 20% 90%;
  --muted-foreground: 220 10% 40%;
  --accent: 28 100% 95%;
  --accent-foreground: 28 100% 40%;
  --destructive: 0 84% 60%;
  --destructive-foreground: 0 0% 100%;
  --radius: 1rem;
}
.dark {
  --background: 220 20% 10%;
  --foreground: 40 33% 98%;
  --border: 220 20% 20%;
  --input: 220 20% 20%;
  --ring: 28 100% 60%;
  --card: 220 20% 15%;
  --card-foreground: 40 33% 98%;
  --popover: 220 20% 15%;
  --popover-foreground: 40 33% 98%;
  --primary: 28 100% 60%;
  --primary-foreground: 0 0% 100%;
  --secondary: 115 89% 35%;
  --secondary-foreground: 0 0% 100%;
  --muted: 220 20% 20%;
  --muted-foreground: 220 10% 70%;
  --accent: 28 100% 20%;
  --accent-foreground: 28 100% 80%;
  --destructive: 0 84% 60%;
  --destructive-foreground: 0 0% 100%;
}
@layer base {
  * { @apply border-border; }
  body { @apply font-sans antialiased bg-background text-foreground; }
}
App.tsx
import { Switch, Route, Router as WouterRouter, useLocation, Redirect } from "wouter";
import { QueryClientProvider } from "@tanstack/react-query";
import { Toaster } from "@/components/ui/toaster";
import { TooltipProvider } from "@/components/ui/tooltip";
import { ClerkProvider, useAuth } from "@clerk/react";
import { queryClient } from "@/lib/queryClient";
import NotFound from "@/pages/not-found";
import Landing from "@/pages/Landing";
import Home from "@/pages/Home";
import Promote from "@/pages/Promote";
import Earnings from "@/pages/Earnings";
import MyChannel from "@/pages/MyChannel";
const clerkPubKey = import.meta.env.VITE_CLERK_PUBLISHABLE_KEY;
const basePath = import.meta.env.BASE_URL.replace(/\/$/, "");
function ProtectedRoute({ component: Component }: { component: React.ComponentType }) {
  const { isSignedIn, isLoaded } = useAuth();
  if (!isLoaded) return null;
  if (!isSignedIn) return <Redirect to="/" />;
  return <Component />;
}
function Router() {
  return (
    <Switch>
      <Route path="/" component={Landing} />
      <Route path="/home">{() => <ProtectedRoute component={Home} />}</Route>
      <Route path="/promote">{() => <ProtectedRoute component={Promote} />}</Route>
      <Route path="/meri-kamayi">{() => <ProtectedRoute component={Earnings} />}</Route>
      <Route path="/mera-channel">{() => <ProtectedRoute component={MyChannel} />}</Route>
      <Route component={NotFound} />
    </Switch>
  );
}
function AppInner() {
  const [, setLocation] = useLocation();
  return (
    <ClerkProvider
      publishableKey={clerkPubKey}
      routerPush={(to) => setLocation(to)}
      routerReplace={(to) => setLocation(to, { replace: true })}
    >
      <TooltipProvider>
        <Router />
        <Toaster />
      </TooltipProvider>
    </ClerkProvider>
  );
}
function App() {
  if (!clerkPubKey) return <div>Missing Clerk Key</div>;
  return (
    <QueryClientProvider client={queryClient}>
      <WouterRouter base={basePath}>
        <AppInner />
      </WouterRouter>
    </QueryClientProvider>
  );
}
export default App;
lib/queryClient.ts
import { QueryClient } from "@tanstack/react-query";
export const queryClient = new QueryClient({
  defaultOptions: {
    queries: { retry: 1, refetchOnWindowFocus: false },
  },
});
components/AdBanner.tsx
import { FC } from "react";
interface AdBannerProps {
  type: "top" | "middle" | "bottom";
}
const AdBanner: FC<AdBannerProps> = ({ type }) => {
  const labelMap = {
    top: "Vigyapan - Top Banner",
    middle: "Vigyapan - Middle Banner",
    bottom: "Vigyapan - Bottom Banner",
  };
  return (
    <div
      data-testid={`ad-banner-${type}`}
      className="w-full flex items-center justify-center p-4 my-2 border-2 border-dashed border-[#D4AF37] bg-yellow-50 text-[#D4AF37] font-semibold text-sm rounded-md shadow-sm"
    >
      {labelMap[type]}
    </div>
  );
};
export default AdBanner;
components/Layout.tsx
import { FC, ReactNode } from "react";
import { Link, useLocation } from "wouter";
import { Home, Compass, IndianRupee, Video } from "lucide-react";
import { useGetMe } from "@workspace/api-client-react";
import AdBanner from "./AdBanner";
interface LayoutProps {
  children: ReactNode;
}
export const Layout: FC<LayoutProps> = ({ children }) => {
  const [location] = useLocation();
  const { data: me } = useGetMe({ query: { queryKey: ["/api/users/me"] } });
  const navItems = [
    { href: "/home", label: "Home", icon: Home },
    { href: "/promote", label: "Promote", icon: Compass },
    { href: "/meri-kamayi", label: "Kamayi", icon: IndianRupee },
    { href: "/mera-channel", label: "Channel", icon: Video },
  ];
  return (
    <div className="mx-auto w-full max-w-md min-h-[100dvh] bg-background shadow-2xl overflow-hidden flex flex-col relative">
      {/* ── Top Ad Banner + Header (sticky) ── */}
      <div className="sticky top-0 z-10 bg-background border-b border-border shadow-sm">
        <AdBanner type="top" />
        <div className="flex items-center justify-between px-4 py-2">
          <span className="font-black text-lg text-primary tracking-tight">VidCoins</span>
          {me !== undefined && (
            <span className="text-xs font-bold bg-primary/10 text-primary px-3 py-1 rounded-full">
              🪙 {me.points} coins
            </span>
          )}
        </div>
      </div>
      {/* ── Page Content ── */}
      <main className="flex-1 overflow-y-auto px-4 py-5 pb-36 scroll-smooth">
        {children}
      </main>
      {/* ── Bottom Ad Banner + Nav (fixed) ── */}
      <div className="absolute bottom-0 w-full bg-background border-t border-border z-20">
        <div className="px-4 pt-2">
          <AdBanner type="bottom" />
        </div>
        <nav className="flex items-center justify-between px-6 py-3 pb-safe text-xs font-medium">
          {navItems.map((item) => {
            const isActive = location === item.href;
            const Icon = item.icon;
            return (
              <Link
                key={item.href}
                href={item.href}
                className={`flex flex-col items-center gap-1 transition-colors ${
                  isActive ? "text-primary" : "text-muted-foreground hover:text-foreground"
                }`}
              >
                <div className={`p-2 rounded-full ${isActive ? "bg-primary/10" : "bg-transparent"}`}>
                  <Icon size={20} strokeWidth={isActive ? 2.5 : 2} />
                </div>
                <span>{item.label}</span>
              </Link>
            );
          })}
        </nav>
      </div>
    </div>
  );
};
pages/Landing.tsx
import { SignInButton, useUser, useAuth } from "@clerk/react";
import { Redirect } from "wouter";
import { useEffect, useRef } from "react";
import { useSyncUser } from "@workspace/api-client-react";
import { Button } from "@/components/ui/button";
export default function Landing() {
  const { user } = useUser();
  const { isSignedIn } = useAuth();
  const syncUser = useSyncUser();
  const hasSynced = useRef(false);
  useEffect(() => {
    if (isSignedIn && user && !hasSynced.current) {
      hasSynced.current = true;
      syncUser.mutate({
        data: {
          clerkId: user.id,
          name: user.fullName || user.username || "User",
          email: user.primaryEmailAddress?.emailAddress || "",
          avatarUrl: user.imageUrl || null,
        },
      });
    }
  }, [isSignedIn, user, syncUser]);
  if (isSignedIn) return <Redirect to="/home" />;
  return (
    <div className="min-h-[100dvh] bg-gradient-to-br from-primary/10 via-background to-secondary/10 flex flex-col items-center justify-center p-6 mx-auto w-full max-w-md">
      <div className="flex flex-col items-center justify-center text-center space-y-8 animate-in fade-in slide-in-from-bottom-4 duration-700">
        <div className="w-24 h-24 bg-white rounded-3xl shadow-xl flex items-center justify-center rotate-3 border-4 border-primary/20">
          <span className="text-4xl font-black text-primary -rotate-3">VC</span>
        </div>
        <div className="space-y-3">
          <h1 className="text-4xl font-black tracking-tight text-foreground">VidCoins</h1>
          <p className="text-lg text-muted-foreground font-medium px-4">
            Video Dekho, Coins Kamao.<br />Apna Channel Promote Karo!
          </p>
        </div>
        <div className="w-full max-w-sm pt-8">
          <SignInButton mode="modal">
            <Button size="lg" className="w-full text-lg h-14 rounded-full shadow-lg hover:shadow-xl transition-all hover:-translate-y-1">
              Start Kamaayi Now
            </Button>
          </SignInButton>
        </div>
      </div>
    </div>
  );
}
pages/Home.tsx
import { useState, useEffect } from "react";
import { Layout } from "@/components/Layout";
import { Input } from "@/components/ui/input";
import { Button } from "@/components/ui/button";
import { Card, CardContent } from "@/components/ui/card";
import { useSearchYoutube, useEarnPoints, useGetMe } from "@workspace/api-client-react";
import { Search, PlayCircle, Loader2, Coins } from "lucide-react";
import { useToast } from "@/hooks/use-toast";
import { queryClient } from "@/lib/queryClient";
import AdBanner from "@/components/AdBanner";
export default function Home() {
  const [channel, setChannel] = useState("");
  const [topic, setTopic] = useState("");
  const [searchParams, setSearchParams] = useState({ q: "trending india" });
  const { data: me } = useGetMe({ query: { queryKey: ["/api/users/me"] } });
  const { data: videos, isLoading } = useSearchYoutube(searchParams, {
    query: { queryKey: ["/api/youtube/search", searchParams] },
  });
  const earnPoints = useEarnPoints();
  const { toast } = useToast();
  const [activeVideo, setActiveVideo] = useState<{ id: string; title: string } | null>(null);
  const [watchSeconds, setWatchSeconds] = useState(0);
  const handleSearch = (e: React.FormEvent) => {
    e.preventDefault();
    const query = `${channel} ${topic}`.trim();
    if (query) setSearchParams({ q: query });
  };
  useEffect(() => {
    let interval: NodeJS.Timeout;
    if (activeVideo && watchSeconds < 10) {
      interval = setInterval(() => setWatchSeconds((prev) => prev + 1), 1000);
    }
    return () => clearInterval(interval);
  }, [activeVideo, watchSeconds]);
  const handleEarn = () => {
    if (!activeVideo) return;
    earnPoints.mutate(
      { data: { videoId: activeVideo.id, videoTitle: activeVideo.title } },
      {
        onSuccess: (res) => {
          toast({ title: "Maza Aa Gaya!", description: `Aapne ${res.earned} coins kamaye hain!` });
          queryClient.invalidateQueries({ queryKey: ["/api/users/me"] });
          setActiveVideo(null);
          setWatchSeconds(0);
        },
      }
    );
  };
  return (
    <Layout>
      <div className="space-y-5">
        {/* Coin Balance Card */}
        <div className="bg-gradient-to-r from-primary/15 to-secondary/10 rounded-2xl p-4 flex items-center justify-between border border-primary/20">
          <div>
            <p className="text-xs text-muted-foreground font-medium uppercase tracking-widest">Aapke Coins</p>
            <p className="text-3xl font-black text-primary leading-tight">{me?.points ?? "—"}</p>
          </div>
          <div className="w-14 h-14 bg-primary/10 rounded-2xl flex items-center justify-center">
            <Coins className="w-7 h-7 text-primary" />
          </div>
        </div>
        {/* Search Panel */}
        <div className="bg-card p-4 rounded-2xl shadow-sm border border-border">
          <h2 className="text-base font-bold mb-3">Video Khojo</h2>
          <form onSubmit={handleSearch} className="space-y-3">
            <Input
              placeholder="Channel Name (e.g. T-Series)"
              value={channel}
              onChange={(e) => setChannel(e.target.value)}
              className="bg-muted/50"
            />
            <Input
              placeholder="Topic (e.g. Cricket, Songs)"
              value={topic}
              onChange={(e) => setTopic(e.target.value)}
              className="bg-muted/50"
            />
            <Button type="submit" className="w-full">
              <Search className="w-4 h-4 mr-2" />
              Search Videos
            </Button>
          </form>
        </div>
        {/* Middle Ad Banner */}
        <AdBanner type="middle" />
        {/* Video Results */}
        <div className="space-y-3">
          <h2 className="text-base font-bold">Results</h2>
          {isLoading ? (
            <div className="flex justify-center py-10">
              <Loader2 className="w-8 h-8 animate-spin text-primary" />
            </div>
          ) : (
            <div className="grid gap-3">
              {videos?.map((video) => (
                <Card
                  key={video.videoId}
                  className="overflow-hidden active:scale-[0.98] transition-transform cursor-pointer"
                  onClick={() => { setActiveVideo({ id: video.videoId, title: video.title }); setWatchSeconds(0); }}
                >
                  <div className="relative">
                    <img src={video.thumbnail} alt={video.title} className="w-full aspect-video object-cover" />
                    <div className="absolute inset-0 bg-black/20 flex items-center justify-center opacity-0 hover:opacity-100 transition-opacity">
                      <PlayCircle className="w-12 h-12 text-white" />
                    </div>
                  </div>
                  <CardContent className="p-3">
                    <h3 className="font-semibold line-clamp-2 text-sm mb-0.5">{video.title}</h3>
                    <p className="text-xs text-muted-foreground">{video.channelTitle}</p>
                  </CardContent>
                </Card>
              ))}
            </div>
          )}
        </div>
      </div>
      {/* Video Player Modal */}
      {activeVideo && (
        <div className="fixed inset-0 z-50 bg-background/95 backdrop-blur flex flex-col p-4">
          <div className="flex-1 flex flex-col justify-center items-center max-w-md mx-auto w-full space-y-4">
            <div className="w-full aspect-video bg-black rounded-xl overflow-hidden shadow-2xl">
              <iframe
                width="100%" height="100%"
                src={`https://www.youtube.com/embed/${activeVideo.id}?autoplay=1`}
                title="YouTube video player"
                frameBorder="0"
                allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture"
                allowFullScreen
              />
            </div>
            <div className="w-full text-center space-y-3">
              <h3 className="font-bold text-base line-clamp-2">{activeVideo.title}</h3>
              {watchSeconds < 10 ? (
                <div className="flex flex-col items-center gap-2">
                  <div className="flex items-center gap-2 text-muted-foreground">
                    <Loader2 className="w-5 h-5 animate-spin text-primary" />
                    <p className="text-sm font-medium">Coins ke liye {10 - watchSeconds} seconds aur dekho...</p>
                  </div>
                  <div className="w-full bg-muted rounded-full h-1.5 mt-1">
                    <div className="bg-primary h-1.5 rounded-full transition-all" style={{ width: `${(watchSeconds / 10) * 100}%` }} />
                  </div>
                </div>
              ) : (
                <Button size="lg" className="w-full rounded-full text-lg animate-in zoom-in" onClick={handleEarn} disabled={earnPoints.isPending}>
                  {earnPoints.isPending ? "Ruko..." : "🪙 Coins Kamao!"}
                </Button>
              )}
            </div>
            <Button variant="ghost" size="sm" className="mt-4 text-muted-foreground" onClick={() => { setActiveVideo(null); setWatchSeconds(0); }}>
              ← Wapas Jao
            </Button>
          </div>
        </div>
      )}
    </Layout>
  );
}
pages/Promote.tsx
import { Layout } from "@/components/Layout";
import { useGetMe, useCreatePromotion, useListPromotions } from "@workspace/api-client-react";
import { Card, CardContent } from "@/components/ui/card";
import { Input } from "@/components/ui/input";
import { Button } from "@/components/ui/button";
import { Label } from "@/components/ui/label";
import { RadioGroup, RadioGroupItem } from "@/components/ui/radio-group";
import { useState } from "react";
import { useToast } from "@/hooks/use-toast";
import { queryClient } from "@/lib/queryClient";
import AdBanner from "@/components/AdBanner";
import { Loader2, TrendingUp, Coins } from "lucide-react";
export default function Promote() {
  const { data: me } = useGetMe({ query: { queryKey: ["/api/users/me"] } });
  const { data: promotions, isLoading } = useListPromotions({ query: { queryKey: ["/api/promotions"] } });
  const createPromotion = useCreatePromotion();
  const { toast } = useToast();
  const [channelName, setChannelName] = useState("");
  const [keywords, setKeywords] = useState("");
  const [pointsCost, setPointsCost] = useState("50");
  const handleSubmit = (e: React.FormEvent) => {
    e.preventDefault();
    if (!channelName || !keywords) return;
    createPromotion.mutate({ data: { channelName, keywords, pointsCost: Number(pointsCost) } }, {
      onSuccess: () => {
        toast({ title: "Badhai Ho!", description: "Aapka channel promotion live ho gaya hai." });
        setChannelName(""); setKeywords("");
        queryClient.invalidateQueries({ queryKey: ["/api/users/me"] });
        queryClient.invalidateQueries({ queryKey: ["/api/promotions"] });
        queryClient.invalidateQueries({ queryKey: ["/api/promotions/mine"] });
      },
      onError: (err: any) => {
        toast({ title: "Error", description: err.message || "Points kam hain ya kuch galat hua.", variant: "destructive" });
      }
    });
  };
  return (
    <Layout>
      <div className="space-y-8 animate-in fade-in slide-in-from-bottom-4 duration-500">
        <div className="bg-gradient-to-r from-primary/20 to-secondary/10 p-6 rounded-3xl text-center shadow-inner border border-primary/20">
          <p className="text-sm font-medium text-muted-foreground
