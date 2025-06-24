import { useState } from "react"; import { Card, CardContent } from "@/components/ui/card"; import { Button } from "@/components/ui/button";

export default function Clikkaza() { const [balance, setBalance] = useState(0); const [clickPower, setClickPower] = useState(1); const [upgradeCost, setUpgradeCost] = useState(50);

const handleClick = () => { setBalance(balance + clickPower); };

const upgradePower = () => { if (balance >= upgradeCost) { setBalance(balance - upgradeCost); setClickPower(clickPower + 1); setUpgradeCost(Math.floor(upgradeCost * 1.5)); } };

return ( <div className="flex flex-col items-center justify-center min-h-screen bg-gray-950 text-white gap-6 p-4"> <h1 className="text-4xl font-bold text-yellow-400">CLIKKAZA</h1> <Card className="bg-gray-800 shadow-xl w-full max-w-md"> <CardContent className="flex flex-col items-center gap-4 p-6"> <div className="text-2xl">💰 G-Баланс: {balance}</div> <Button onClick={handleClick} className="text-xl px-8 py-4 bg-yellow-500 hover:bg-yellow-600"> КЛИКНИ МНЕ, СУКА </Button> <div className="text-md">⚡ Сила клика: {clickPower}</div> <Button onClick={upgradePower} disabled={balance < upgradeCost} className="mt-2 px-6 py-2 bg-purple-600 hover:bg-purple-700"> Прокачать силу ({upgradeCost} G$) </Button> </CardContent> </Card> </div> ); }

import { useState } from "react"; import { Card, CardContent } from "@/components/ui/card"; import { Button } from "@/components/ui/button";

export default function Clikkaza() { const [balance, setBalance] = useState(0); const [clickPower, setClickPower] = useState(1); const [upgradeCost, setUpgradeCost] = useState(50);

const handleClick = () => { setBalance(balance + clickPower); };

const upgradePower = () => { if (balance >= upgradeCost) { setBalance(balance - upgradeCost); setClickPower(clickPower + 1); setUpgradeCost(Math.floor(upgradeCost * 1.5)); } };

return ( <div className="flex flex-col items-center justify-center min-h-screen bg-gray-950 text-white gap-6 p-4"> <h1 className="text-4xl font-bold text-yellow-400">CLIKKAZA</h1> <Card className="bg-gray-800 shadow-xl w-full max-w-md"> <CardContent className="flex flex-col items-center gap-4 p-6"> <div className="text-2xl">💰 G-Баланс: {balance}</div> <Button onClick={handleClick} className="text-xl px-8 py-4 bg-yellow-500 hover:bg-yellow-600"> КЛИКНИ МНЕ, СУКА </Button> <div className="text-md">⚡ Сила клика: {clickPower}</div> <Button onClick={upgradePower} disabled={balance < upgradeCost} className="mt-2 px-6 py-2 bg-purple-600 hover:bg-purple-700"> Прокачать силу ({upgradeCost} G$) </Button> </CardContent> </Card> </div> ); }

