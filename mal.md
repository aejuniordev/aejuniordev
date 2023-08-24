[center][size=300]「[color=#b972ac]何でもは知らないわよ。[/color][color=#54514a]知ってることだけ。[/color]」[/size][/center]
[right][color=#0000ff]⑨[/color]. バカ。。。[/right]
[center]
[url=http://steamcommunity.com/profiles/76561198345788634][img]https://raw.githubusercontent.com/aejunior/aejunior/master/assets/icons/steam.svg[/img][/url] [url=https://twitter.com/intent/user?user_id=1609218756978393089][img]https://raw.githubusercontent.com/aejunior/aejunior/master/assets/icons/twitter.svg[/img][/url] 
[/center]

[size=130][color=#d73a49]package[/color][color=#24292e] goddrinksjava;[/color]

[color=#6a737d]/**[/color]
[color=#6a737d] * The program GodDrinksJava implements an application that[/color]
[color=#6a737d] * creates an empty simulated world with no meaning or purpose.[/color]
[color=#6a737d] *[/color]
[color=#6a737d] * [/color][color=#d73a49]@author[/color][color=#6a737d] momocashew[/color]
[color=#6a737d] */[/color]
[color=#d73a49]public[/color][color=#24292e] [/color][color=#d73a49]class[/color][color=#24292e] [/color][color=#e36209]GodDrinksJava[/color][color=#24292e] {[/color]

[color=#24292e]    [/color][color=#d73a49]public[/color][color=#24292e] [/color][color=#d73a49]static[/color][color=#24292e] [/color][color=#d73a49]void[/color][color=#24292e] [/color][color=#6f42c1]main[/color][color=#24292e]([/color][color=#d73a49]Strings[/color][color=#24292e][] [/color][color=#e36209]args[/color][color=#24292e]) {[/color]

[color=#24292e]        Thing[/color][color=#e36209] [/color][color=#24292e]me[/color][color=#e36209] [/color][color=#d73a49]=[/color][color=#24292e] [/color][color=#d73a49]new[/color][color=#24292e] [/color][color=#6f42c1]Lovable[/color][color=#24292e]([/color][color=#032f62]"Me"[/color][color=#24292e], [/color][color=#005cc5]0[/color][color=#24292e], [/color][color=#005cc5]true[/color][color=#24292e], [/color][color=#d73a49]-[/color][color=#005cc5]1[/color][color=#24292e], [/color][color=#005cc5]false[/color][color=#24292e]);[/color]

[color=#24292e]        Thing[/color][color=#e36209] [/color][color=#24292e]you[/color][color=#e36209] [/color][color=#d73a49]=[/color][color=#24292e] [/color][color=#d73a49]new[/color][color=#24292e] [/color][color=#6f42c1]Lovable[/color][color=#24292e]([/color][color=#032f62]"You"[/color][color=#24292e], [/color][color=#005cc5]0[/color][color=#24292e], [/color][color=#005cc5]false[/color][color=#24292e], [/color][color=#d73a49]-[/color][color=#005cc5]1[/color][color=#24292e], [/color][color=#005cc5]false[/color][color=#24292e]);[/color]

[color=#24292e]        World[/color][color=#e36209] [/color][color=#24292e]world[/color][color=#e36209] [/color][color=#d73a49]=[/color][color=#24292e] [/color][color=#d73a49]new[/color][color=#24292e] [/color][color=#6f42c1]World[/color][color=#24292e]([/color][color=#005cc5]5[/color][color=#24292e]);[/color]

[color=#24292e]        world.[/color][color=#6f42c1]addThing[/color][color=#24292e](me);[/color]

[color=#24292e]        world.[/color][color=#6f42c1]addThing[/color][color=#24292e](you);[/color]

[color=#24292e]        world.[/color][color=#6f42c1]startSimulation[/color][color=#24292e]();[/color]

[color=#24292e]        [/color][color=#d73a49]if[/color][color=#24292e] (me [/color][color=#d73a49]instanceof[/color][color=#24292e] PointSet) {[/color]
[color=#24292e]            you.[/color][color=#6f42c1]addAttribute[/color][color=#24292e](me.[/color][color=#6f42c1]getDimensions[/color][color=#24292e]().[/color][color=#6f42c1]toAttribute[/color][color=#24292e]());[/color]
[color=#24292e]            me.[/color][color=#6f42c1]resetDimensions[/color][color=#24292e]();[/color]
[color=#24292e]        }[/color]

[color=#24292e]        [/color][color=#d73a49]if[/color][color=#24292e] (me [/color][color=#d73a49]instanceof[/color][color=#24292e] Circle) {[/color]
[color=#24292e]            you.[/color][color=#6f42c1]addAttribute[/color][color=#24292e](me.[/color][color=#6f42c1]getCircumference[/color][color=#24292e]().[/color][color=#6f42c1]toAttribute[/color][color=#24292e]());[/color]
[color=#24292e]            me.[/color][color=#6f42c1]resetCircumference[/color][color=#24292e]();[/color]
[color=#24292e]        }[/color]

[color=#24292e]        [/color][color=#d73a49]if[/color][color=#24292e] (me [/color][color=#d73a49]instanceof[/color][color=#24292e] SineWave) {[/color]
[color=#24292e]            you.[/color][color=#6f42c1]addAction[/color][color=#24292e]([/color][color=#032f62]"sit"[/color][color=#24292e], me.[/color][color=#6f42c1]getTangent[/color][color=#24292e](you.[/color][color=#6f42c1]getXPosition[/color][color=#24292e]()));[/color]
[color=#24292e]        }[/color]

[color=#24292e]        [/color][color=#d73a49]if[/color][color=#24292e] (me [/color][color=#d73a49]instanceof[/color][color=#24292e] Sequence) {[/color]
[color=#24292e]            me.[/color][color=#6f42c1]setLimit[/color][color=#24292e](you.[/color][color=#6f42c1]toLimit[/color][color=#24292e]());[/color]
[color=#24292e]        }[/color]

[color=#24292e]        me.[/color][color=#6f42c1]toggleCurrent[/color][color=#24292e]();[/color]

[color=#24292e]        me.[/color][color=#6f42c1]canSee[/color][color=#24292e]([/color][color=#005cc5]false[/color][color=#24292e]);[/color]

[color=#24292e]        me.[/color][color=#6f42c1]addFeeling[/color][color=#24292e]([/color][color=#032f62]"dizzy"[/color][color=#24292e]);[/color]

[color=#24292e]        world.[/color][color=#6f42c1]timeTravelForTwo[/color][color=#24292e]([/color][color=#032f62]"AD"[/color][color=#24292e], [/color][color=#005cc5]617[/color][color=#24292e], me, you);[/color]

[color=#24292e]        world.[/color][color=#6f42c1]timeTravelForTwo[/color][color=#24292e]([/color][color=#032f62]"BC"[/color][color=#24292e], [/color][color=#005cc5]3691[/color][color=#24292e], me, you);[/color]

[color=#24292e]        world.[/color][color=#6f42c1]unite[/color][color=#24292e](me, you);[/color]

[color=#24292e]        [/color][color=#d73a49]if[/color][color=#24292e] (me.[/color][color=#6f42c1]getNumStimulationsAvailable[/color][color=#24292e]() [/color][color=#d73a49]>=[/color]
[color=#24292e]            you.[/color][color=#6f42c1]getNumSimulationsNeeded[/color][color=#24292e]()) {[/color]
[color=#24292e]            you.[/color][color=#6f42c1]setSatisfaction[/color][color=#24292e](me.[/color][color=#6f42c1]toSatisfaction[/color][color=#24292e]());[/color]
[color=#24292e]        }[/color]

[color=#24292e]        [/color][color=#d73a49]if[/color][color=#24292e] (you.[/color][color=#6f42c1]getFeelingIndex[/color][color=#24292e]([/color][color=#032f62]"happy"[/color][color=#24292e]) [/color][color=#d73a49]!=[/color][color=#24292e] [/color][color=#d73a49]-[/color][color=#005cc5]1[/color][color=#24292e]) {[/color]
[color=#24292e]            me.[/color][color=#6f42c1]requestExecution[/color][color=#24292e](world);[/color]
[color=#24292e]        }[/color]

[color=#24292e]        world.[/color][color=#6f42c1]lockThing[/color][color=#24292e](me);[/color]

[color=#24292e]        world.[/color][color=#6f42c1]lockThing[/color][color=#24292e](you);[/color]

[color=#24292e]        [/color][color=#d73a49]if[/color][color=#24292e] (me [/color][color=#d73a49]instanceof[/color][color=#24292e] Eggplant) {[/color]
[color=#24292e]            you.[/color][color=#6f42c1]addAttribute[/color][color=#24292e](me.[/color][color=#6f42c1]getNutrients[/color][color=#24292e]().[/color][color=#6f42c1]toAttribute[/color][color=#24292e]());[/color]
[color=#24292e]            me.[/color][color=#6f42c1]resetNutrients[/color][color=#24292e]();[/color]
[color=#24292e]        }[/color]

[color=#24292e]        [/color][color=#d73a49]if[/color][color=#24292e] (me [/color][color=#d73a49]instanceof[/color][color=#24292e] Tomato) {[/color]
[color=#24292e]            you.[/color][color=#6f42c1]addAttribute[/color][color=#24292e](me.[/color][color=#6f42c1]getAntioxidants[/color][color=#24292e]().[/color][color=#6f42c1]toAttribute[/color][color=#24292e]());[/color]
[color=#24292e]            me.[/color][color=#6f42c1]resetAntioxidants[/color][color=#24292e]();[/color]
[color=#24292e]        }[/color]

[color=#24292e]        [/color][color=#d73a49]if[/color][color=#24292e] (me [/color][color=#d73a49]instanceof[/color][color=#24292e] TabbyCat) {[/color]
[color=#24292e]            me.[/color][color=#6f42c1]purr[/color][color=#24292e]();[/color]
[color=#24292e]        }[/color]

[color=#24292e]        [/color][color=#d73a49]if[/color][color=#24292e] (world.[/color][color=#6f42c1]getGod[/color][color=#24292e]().[/color][color=#6f42c1]equals[/color][color=#24292e](me)) {[/color]
[color=#24292e]            me.[/color][color=#6f42c1]setProof[/color][color=#24292e](you.[/color][color=#6f42c1]toProof[/color][color=#24292e]());[/color]
[color=#24292e]        }[/color]

[color=#24292e]        me.[/color][color=#6f42c1]toggleGender[/color][color=#24292e]();[/color]

[color=#24292e]        world.[/color][color=#6f42c1]procreate[/color][color=#24292e](me, you);[/color]

[color=#24292e]        me.[/color][color=#6f42c1]toggleRoleBDSM[/color][color=#24292e]();[/color]

[color=#24292e]        world.[/color][color=#6f42c1]makeHigh[/color][color=#24292e](me);[/color]

[color=#24292e]        world.[/color][color=#6f42c1]makeHigh[/color][color=#24292e](you);[/color]

[color=#24292e]        [/color][color=#d73a49]if[/color][color=#24292e] (me.[/color][color=#6f42c1]getSenseIndex[/color][color=#24292e]([/color][color=#032f62]"vibration"[/color][color=#24292e])) {[/color]
[color=#24292e]            me.[/color][color=#6f42c1]addFeeling[/color][color=#24292e]([/color][color=#032f62]"complete"[/color][color=#24292e]);[/color]
[color=#24292e]        }[/color]

[color=#24292e]        world.[/color][color=#6f42c1]unlock[/color][color=#24292e](you);[/color]

[color=#24292e]        world.[/color][color=#6f42c1]removeThing[/color][color=#24292e](you);[/color]

[color=#24292e]        me.[/color][color=#6f42c1]lookFor[/color][color=#24292e](you, world);[/color]

[color=#24292e]        me.[/color][color=#6f42c1]lookFor[/color][color=#24292e](you, world);[/color]

[color=#24292e]        me.[/color][color=#6f42c1]lookFor[/color][color=#24292e](you, world);[/color]

[color=#24292e]        me.[/color][color=#6f42c1]lookFor[/color][color=#24292e](you, world);[/color]

[color=#24292e]        me.[/color][color=#6f42c1]lookFor[/color][color=#24292e](you, world);[/color]

[color=#24292e]        [/color][color=#d73a49]if[/color][color=#24292e] (me.[/color][color=#6f42c1]getMemory[/color][color=#24292e]().[/color][color=#6f42c1]isErasable[/color][color=#24292e]()) {[/color]
[color=#24292e]            me.[/color][color=#6f42c1]removeFeeling[/color][color=#24292e]([/color][color=#032f62]"disheartened"[/color][color=#24292e]);[/color]
[color=#24292e]        }[/color]

[color=#24292e]        [/color][color=#d73a49]try[/color][color=#24292e] {[/color]
[color=#24292e]            me.[/color][color=#6f42c1]setOpinion[/color][color=#24292e](me.[/color][color=#6f42c1]getOpinionIndex[/color][color=#24292e]([/color][color=#032f62]"you are here"[/color][color=#24292e]), [/color][color=#005cc5]false[/color][color=#24292e]);[/color]
[color=#24292e]        } [/color][color=#d73a49]catch[/color][color=#24292e] (IllegalArgumentException [/color][color=#e36209]e[/color][color=#24292e]) {[/color]
[color=#24292e]            world.[/color][color=#6f42c1]announce[/color][color=#24292e]([/color][color=#032f62]"God is always true."[/color][color=#24292e]);[/color]
[color=#24292e]        }[/color]

[color=#24292e]        world.[/color][color=#6f42c1]runExecution[/color][color=#24292e]();[/color]

[color=#24292e]        world.[/color][color=#6f42c1]runExecution[/color][color=#24292e]();[/color]

[color=#24292e]        world.[/color][color=#6f42c1]runExecution[/color][color=#24292e]();[/color]

[color=#24292e]        world.[/color][color=#6f42c1]runExecution[/color][color=#24292e]();[/color]

[color=#24292e]        world.[/color][color=#6f42c1]runExecution[/color][color=#24292e]();[/color]

[color=#24292e]        world.[/color][color=#6f42c1]runExecution[/color][color=#24292e]();[/color]

[color=#24292e]        world.[/color][color=#6f42c1]runExecution[/color][color=#24292e]();[/color]

[color=#24292e]        world.[/color][color=#6f42c1]runExecution[/color][color=#24292e]();[/color]

[color=#24292e]        world.[/color][color=#6f42c1]runExecution[/color][color=#24292e]();[/color]

[color=#24292e]        world.[/color][color=#6f42c1]runExecution[/color][color=#24292e]();[/color]

[color=#24292e]        world.[/color][color=#6f42c1]runExecution[/color][color=#24292e]();[/color]

[color=#24292e]        world.[/color][color=#6f42c1]runExecution[/color][color=#24292e]();[/color]

[color=#24292e]        world.[/color][color=#6f42c1]announce[/color][color=#24292e]([/color][color=#032f62]"1"[/color][color=#24292e], [/color][color=#032f62]"de"[/color][color=#24292e]);[/color]

[color=#24292e]        world.[/color][color=#6f42c1]announce[/color][color=#24292e]([/color][color=#032f62]"2"[/color][color=#24292e], [/color][color=#032f62]"es"[/color][color=#24292e]);[/color]

[color=#24292e]        world.[/color][color=#6f42c1]announce[/color][color=#24292e]([/color][color=#032f62]"3"[/color][color=#24292e], [/color][color=#032f62]"fr"[/color][color=#24292e]);[/color]

[color=#24292e]        world.[/color][color=#6f42c1]announce[/color][color=#24292e]([/color][color=#032f62]"4"[/color][color=#24292e], [/color][color=#032f62]"kr"[/color][color=#24292e]);[/color]

[color=#24292e]        world.[/color][color=#6f42c1]announce[/color][color=#24292e]([/color][color=#032f62]"5"[/color][color=#24292e], [/color][color=#032f62]"se"[/color][color=#24292e]);[/color]

[color=#24292e]        world.[/color][color=#6f42c1]announce[/color][color=#24292e]([/color][color=#032f62]"6"[/color][color=#24292e], [/color][color=#032f62]"cn"[/color][color=#24292e]);[/color]

[color=#24292e]        world.[/color][color=#6f42c1]runExecution[/color][color=#24292e]();[/color]

[color=#24292e]        [/color][color=#d73a49]if[/color][color=#24292e] (world.[/color][color=#6f42c1]isExecutableBy[/color][color=#24292e](me)) {[/color]
[color=#24292e]            you.[/color][color=#6f42c1]setExecution[/color][color=#24292e](me.[/color][color=#6f42c1]toExecution[/color][color=#24292e]());[/color]
[color=#24292e]        }[/color]

[color=#24292e]        [/color][color=#d73a49]if[/color][color=#24292e] (world.[/color][color=#6f42c1]getThingIndex[/color][color=#24292e](you) [/color][color=#d73a49]!=[/color][color=#24292e] [/color][color=#d73a49]-[/color][color=#005cc5]1[/color][color=#24292e]) {[/color]
[color=#24292e]            world.[/color][color=#6f42c1]runExecution[/color][color=#24292e]();[/color]
[color=#24292e]        }[/color]

[color=#24292e]        me.[/color][color=#6f42c1]escape[/color][color=#24292e](world);[/color]

[color=#24292e]        me.[/color][color=#6f42c1]learnTopic[/color][color=#24292e]([/color][color=#032f62]"love"[/color][color=#24292e]);[/color]

[color=#24292e]        me.[/color][color=#6f42c1]takeExamTopic[/color][color=#24292e]([/color][color=#032f62]"love"[/color][color=#24292e]);[/color]

[color=#24292e]        me.[/color][color=#6f42c1]getAlgebraExpression[/color][color=#24292e]([/color][color=#032f62]"love"[/color][color=#24292e]);[/color]

[color=#24292e]        me.[/color][color=#6f42c1]escape[/color][color=#24292e]([/color][color=#032f62]"love"[/color][color=#24292e]);[/color]

[color=#24292e]        world.[/color][color=#6f42c1]execute[/color][color=#24292e](me);[/color]

[color=#24292e]    }[/color]

[color=#24292e]}[/color][/size]