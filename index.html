// Full Spirit Mode Mental Math Supertrainer with All Modes Active
import React, { useState, useEffect } from "react";
import { Tabs, TabsList, TabsTrigger, TabsContent } from "@/components/ui/tabs";
import { Card, CardContent } from "@/components/ui/card";
import { Button } from "@/components/ui/button";
import { Slider } from "@/components/ui/slider";

function getRandomDigits(length) {
  return Array.from({ length }, () => Math.floor(Math.random() * 10)).join("");
}

function getRandom2Digit() {
  return Math.floor(Math.random() * 90 + 10);
}

function getRandomMultiplier(length) {
  return Math.floor(Math.random() * (10 ** length - 10 ** (length - 1)) + 10 ** (length - 1));
}

export default function SpiritModeTrainer() {
  const [mode, setMode] = useState("digit-span");

  // Shared States
  const [digits, setDigits] = useState(7);
  const [flashTime, setFlashTime] = useState(500);
  const [numbersCount, setNumbersCount] = useState(10);
  const [userInput, setUserInput] = useState("");
  const [result, setResult] = useState(null);

  // Digit Span
  const [generatedDigits, setGeneratedDigits] = useState("");
  const [showDigits, setShowDigits] = useState(false);

  useEffect(() => {
    if (showDigits) {
      const timeout = setTimeout(() => setShowDigits(false), flashTime);
      return () => clearTimeout(timeout);
    }
  }, [showDigits, flashTime]);

  const startDigitSpan = () => {
    setGeneratedDigits(getRandomDigits(digits));
    setShowDigits(true);
    setUserInput("");
    setResult(null);
  };

  const checkDigitSpan = () => {
    setResult(userInput === generatedDigits ? "Correct" : "Wrong");
  };

  // Flash Anzan
  const [anzanNumbers, setAnzanNumbers] = useState([]);
  const [currentIndex, setCurrentIndex] = useState(0);
  const [anzanSum, setAnzanSum] = useState(0);
  const [showAnzan, setShowAnzan] = useState(false);

  const startFlashAnzan = () => {
    const nums = Array.from({ length: numbersCount }, () => getRandom2Digit());
    setAnzanNumbers(nums);
    setAnzanSum(nums.reduce((a, b) => a + b, 0));
    setCurrentIndex(0);
    setShowAnzan(true);
    setUserInput("");
    setResult(null);
  };

  useEffect(() => {
    if (showAnzan && currentIndex < anzanNumbers.length) {
      const timer = setTimeout(() => setCurrentIndex(i => i + 1), flashTime);
      return () => clearTimeout(timer);
    }
    if (currentIndex >= anzanNumbers.length) setShowAnzan(false);
  }, [showAnzan, currentIndex, flashTime, anzanNumbers.length]);

  const checkAnzanAnswer = () => {
    setResult(parseInt(userInput) === anzanSum ? "Correct" : `Wrong. Answer: ${anzanSum}`);
  };

  // Multiplication
  const [multA, setMultA] = useState(0);
  const [multB, setMultB] = useState(0);
  const [multAnswer, setMultAnswer] = useState(0);

  const startMultiplication = () => {
    const a = getRandomMultiplier(2);
    const b = getRandomMultiplier(2);
    setMultA(a);
    setMultB(b);
    setMultAnswer(a * b);
    setUserInput("");
    setResult(null);
  };

  const checkMultiplication = () => {
    setResult(parseInt(userInput) === multAnswer ? "Correct" : `Wrong. Answer: ${multAnswer}`);
  };

  // Memory Stack (recall + solve)
  const [memStackDigits, setMemStackDigits] = useState("");
  const [memMathQ, setMemMathQ] = useState({ a: 0, b: 0 });
  const [showMemStackPhase, setShowMemStackPhase] = useState("flash");

  const startMemoryStack = () => {
    setMemStackDigits(getRandomDigits(4));
    setMemMathQ({ a: getRandom2Digit(), b: getRandom2Digit() });
    setShowMemStackPhase("flash");
    setTimeout(() => setShowMemStackPhase("math"), flashTime);
    setUserInput("");
    setResult(null);
  };

  const checkMemoryStack = () => {
    setResult(userInput === memStackDigits ? "Correct" : `Wrong. It was ${memStackDigits}`);
  };

  // Reaction Mode
  const [reactionTarget, setReactionTarget] = useState("");
  const [reactionStart, setReactionStart] = useState(null);
  const [reactionTime, setReactionTime] = useState(null);

  const startReaction = () => {
    setReactionTarget("");
    setReactionTime(null);
    setUserInput("");
    const timeout = setTimeout(() => {
      const target = getRandomDigits(3);
      setReactionTarget(target);
      setReactionStart(Date.now());
    }, Math.random() * 3000 + 1000);
    return () => clearTimeout(timeout);
  };

  const checkReaction = () => {
    const time = Date.now() - reactionStart;
    setReactionTime(`${time} ms`);
    setResult(userInput === reactionTarget ? "Correct" : `Wrong. It was ${reactionTarget}`);
  };

  return (
    <div className="min-h-screen bg-black text-green-500 p-6 font-mono">
      <h1 className="text-4xl font-bold mb-6 text-center">SPIRIT MODE: Mental Math Supertrainer</h1>
      <Tabs value={mode} onValueChange={setMode}>
        <TabsList className="flex justify-center gap-4 mb-6">
          <TabsTrigger value="digit-span">Digit Span</TabsTrigger>
          <TabsTrigger value="flash-anzan">Flash Anzan</TabsTrigger>
          <TabsTrigger value="multiplication">Multiplication</TabsTrigger>
          <TabsTrigger value="memory-stack">Memory Stack</TabsTrigger>
          <TabsTrigger value="reaction">Reaction</TabsTrigger>
        </TabsList>

        <TabsContent value="digit-span">
          <Card><CardContent className="p-4 space-y-4">
            <h2 className="text-2xl font-semibold">Digit Span</h2>
            <Slider value={[digits]} onValueChange={([v]) => setDigits(v)} min={3} max={20} />
            <Slider value={[flashTime]} onValueChange={([v]) => setFlashTime(v)} min={100} max={1000} />
            <Button onClick={startDigitSpan}>Start</Button>
            {showDigits && <div className="text-3xl text-center">{generatedDigits}</div>}
            {!showDigits && generatedDigits && (
              <><input value={userInput} onChange={(e) => setUserInput(e.target.value)} className="text-xl w-full" /><Button onClick={checkDigitSpan}>Check</Button><div>{result}</div></>
            )}
          </CardContent></Card>
        </TabsContent>

        <TabsContent value="flash-anzan">
          <Card><CardContent className="p-4 space-y-4">
            <h2 className="text-2xl font-semibold">Flash Anzan</h2>
            <Slider value={[numbersCount]} onValueChange={([v]) => setNumbersCount(v)} min={3} max={30} />
            <Slider value={[flashTime]} onValueChange={([v]) => setFlashTime(v)} min={100} max={1000} />
            <Button onClick={startFlashAnzan}>Start</Button>
            {showAnzan && currentIndex < anzanNumbers.length && <div className="text-3xl text-center">{anzanNumbers[currentIndex]}</div>}
            {!showAnzan && anzanNumbers.length > 0 && (
              <><input value={userInput} onChange={(e) => setUserInput(e.target.value)} className="text-xl w-full" /><Button onClick={checkAnzanAnswer}>Check</Button><div>{result}</div></>
            )}
          </CardContent></Card>
        </TabsContent>

        <TabsContent value="multiplication">
          <Card><CardContent className="p-4 space-y-4">
            <h2 className="text-2xl font-semibold">Multiplication</h2>
            <Button onClick={startMultiplication}>New Problem</Button>
            {multA > 0 && multB > 0 && <div className="text-3xl text-center">{multA} × {multB}</div>}
            {multA > 0 && (
              <><input value={userInput} onChange={(e) => setUserInput(e.target.value)} className="text-xl w-full" /><Button onClick={checkMultiplication}>Check</Button><div>{result}</div></>
            )}
          </CardContent></Card>
        </TabsContent>

        <TabsContent value="memory-stack">
          <Card><CardContent className="p-4 space-y-4">
            <h2 className="text-2xl font-semibold">Memory Stack</h2>
            <Button onClick={startMemoryStack}>Start</Button>
            {showMemStackPhase === "flash" && <div className="text-3xl text-center">{memStackDigits}</div>}
            {showMemStackPhase === "math" && (
              <>
                <div className="text-xl">Now solve: {memMathQ.a} + {memMathQ.b}</div>
                <input value={userInput} onChange={(e) => setUserInput(e.target.value)} className="text-xl w-full" />
                <Button onClick={checkMemoryStack}>Recall Digits</Button>
                <div>{result}</div>
              </>
            )}
          </CardContent></Card>
        </TabsContent>

        <TabsContent value="reaction">
          <Card><CardContent className="p-4 space-y-4">
            <h2 className="text-2xl font-semibold">Reaction Challenge</h2>
            <Button onClick={startReaction}>Start</Button>
            {reactionTarget && <div className="text-3xl text-center">{reactionTarget}</div>}
            {reactionTarget && (
              <><input value={userInput} onChange={(e) => setUserInput(e.target.value)} className="text-xl w-full" /><Button onClick={checkReaction}>Check</Button><div>{result} ({reactionTime})</div></>
            )}
          </CardContent></Card>
        </TabsContent>

      </Tabs>
    </div>
  );
}
