[

   
	//personal
    {trigger: "stack",replacement: "\\stackrel{$0}{$1} $2",options: "mA"},
    {trigger: "?=",replacement: "\\stackrel{?}{=} \ $0",options: "mA"},
    {trigger: "lr=",replacement: "\\Leftrightarrow \ $0",options: "mA"},
    {trigger: "lr-",replacement: "\\leftrightarrow \ $0",options: "mA"},
    {trigger: "l-",replacement: "\\leftarrow \ $0",options: "mA"},
    {trigger: "l=",replacement: "\\Leftarrow \ $0",options: "mA"},
    {trigger: "<-",replacement: "\\leftarrow \ $0",options: "mA"},
    {trigger: "-<",replacement: "\\leftarrow \ $0",options: "mA"},
    {trigger: "r-",replacement: "\\rightarrow  \ $0",options: "mA"},
    {trigger: "uar",replacement: "\\uparrow \ $0",options: "mA"},
    {trigger: "dar",replacement: "\\downarrow \ $0",options: "mA"},
    
    {trigger: "r=",replacement: "\\Rightarrow \ $0",options: "mA"},
    {trigger: "->",replacement: "\\rightarrow \ $0",options: "mA"},
    {trigger: "tra",replacement: "\\xrightarrow {$0}\ $1",options: "mA"},
    {trigger: "tla",replacement: "\\xleftarrow {$0}\ $1",options: "mA"},
    {trigger: "subeq",replacement: "\\subseteq \ $0", priority:0, options: "mA"},
    
    {trigger: "net",replacement: "_{net} \ ",priority:0,options: "mA"},
    {trigger: "}net",replacement: "}_{net} \ ",priority:0,options: "mA"},
    {trigger: "mag",replacement: "\\left| $0 \\right| $1",options: "mA"},
    {trigger: "lb",replacement: "\\left| $0  ",options: "mA"},
    {trigger: "rb",replacement: "\\right| $0",options: "mA"},
    
    {trigger: "big|",replacement: "\\bigg|_{$0}^{$1} $2 ",options: "mA"},
    {trigger: "big |",replacement: "\\bigg| $0",options: "mA"},
    {trigger: "ibar",replacement: "\\bigg| $0",options: "mA", priority:1},

    {trigger: "forall",replacement: "\\forall ",options: "mA"},
    {trigger: "exists",replacement: "\\exists",options: "mA"},
    {trigger: "in",replacement: "\\in \ $0",options: "m"},
    {trigger: "ni",replacement: "\\ni \ $0",options: "mA"},
    
    {trigger: "Rl",replacement: "\\mathbb{R} $0",priority:2,options: "mA"},
    {trigger: "Rm",replacement: "\\mathbb{R}^{m} $0",priority:2,options: "mA"},
    {trigger: "Rn",replacement: "\\mathbb{R}^{n} $0",priority:2,options: "mA"},
    {trigger: "nn",replacement: "_{n}",options: "mA"},
    {trigger: "Fnn",replacement: "F_{n}",options: "mA"},
    {trigger: "Vnn",replacement: "V_{n}",options: "mA"},
    {trigger: "Unn",replacement: "U_{n}",options: "mA"},
    {trigger: "fnn",replacement: "f_{n}",options: "mA"},
    {trigger: "vnn",replacement: "v_{n}",options: "mA"},
    {trigger: "unn",replacement: "u_{n}",options: "mA"},
    {trigger: ")kk",replacement: ")_{k}",options: "mA"},
    {trigger: ")uu",replacement: ")_{u}",options: "mA"},
    {trigger: ")nn",replacement: ")_{n}",options: "mA"},
    {trigger: "}kk",replacement: "}_{k}",options: "mA"},
    {trigger: "}uu",replacement: "}_{u}",options: "mA"},
    {trigger: "}nn",replacement: "}_{n}",options: "mA"},

    {trigger: "Fii",replacement: "F_{i}",options: "mA"},
    {trigger: "Vii",replacement: "V_{i}",options: "mA"},
    {trigger: "Uii",replacement: "U_{i}",options: "mA"},
    {trigger: "fii",replacement: "f_{i}",options: "mA"},
    {trigger: "vii",replacement: "v_{i}",options: "mA"},
    {trigger: "uii",replacement: "u_{i}",options: "mA"},

    {trigger: "Fjj",replacement: "F_{j}",options: "mA"},
    {trigger: "Vjj",replacement: "V_{j}",options: "mA"},
    {trigger: "Ujj",replacement: "U_{j}",options: "mA"},
    {trigger: "fjj",replacement: "f_{j}",options: "mA"},
    {trigger: "vjj",replacement: "v_{j}",options: "mA"},
    {trigger: "ujj",replacement: "u_{j}",options: "mA"},

    
    {trigger: "xx",replacement: "\\vec{x}",options: "mA"},
    {trigger: "vv",replacement: "\\vec{v}",options: "mA"},
    {trigger: "rr",replacement: "\\vec{r}",options: "mA"},
    {trigger: "uu",replacement: "\\vec{u}",options: "mA"},
    {trigger: "pp",replacement: "\\vec{p}",options: "mA"},
    {trigger: "aa",replacement: "\\vec{a}",options: "mA"},
    {trigger: "bb",replacement: "\\vec{b}",options: "mA"},
    {trigger: "cc",replacement: "\\vec{c}",options: "mA"},
    {trigger: "ff",replacement: "\\vec{f}",options: "mA"},
    {trigger: "FF",replacement: "\\vec{F}",options: "mA"},
    {trigger: "00",replacement: "\\vec{0}",options: "mA"},
    
    {trigger: "yy",replacement: "\\vec{y}",options: "mA"},
    {trigger: "dt",replacement: "\\frac{d$0}{dt}$1",options: "m"},
    {trigger: "dx",replacement: "\\frac{d$0}{dx}$1",options: "m"},
    {trigger: "dy",replacement: "\\frac{d$0}{dy}$1",options: "m"},
    
    {trigger: "tot",replacement: "_{tot} $0",options: "mA"},
    {trigger: "cm",replacement: "_{cm} $0",options: "mA"},
    
    {trigger: "sp",replacement: "\\, $0",priority:0,description:"space in math mod ",options: "m"},
    {trigger: "and",replacement: "\\text{ and }  $0",priority:0,options: "mA"},
    {trigger: "\nu \ll ",replacement: "null($0) $1",priority:0,options: "mA"},

    
    
    {trigger: "o\right| ",replacement: "orb",priority:0,options: "A"},
    {trigger: "or ",replacement: "\\text{ or }  $0",priority:0,options: "mA"},

    {trigger: "choose",replacement: "\\choose  $0",priority:0,options: "mA"},
    
    //logic:
    {trigger: "llcorn",replacement: "\\llcorner $0", priority:0, options: "mA"},
     {trigger: "\ll corn",replacement: "\llcorner $0", priority:0, options: "mA"},
    {trigger: "lrcorn",replacement: "\\lrcorner $0", priority:0, options: "mA"},
    {trigger: "ulcorn",replacement: "\\ulcorner $0", priority:0, options: "mA"},
    {trigger: "urcorn",replacement: "\\urcorner $0", priority:0, options: "mA"},
    //text
    {trigger: "tbb",replacement: "\\mathbb{$0} $1", priority:0, options: "mA"},
    
    //physics
    
    {trigger: "\to_{1}",replacement: "\\to 1 $0",options: "mA"},
    {trigger: "\to_{2}",replacement: "\\to 2 $0",options: "mA"},
    {trigger: "\to_{3}",replacement: "\\to 3 $0",options: "mA"},
    //non math personal
    {trigger: "collab ",replacement: "Collaborators: $0",priority:0,options: "A"},
    {trigger: "ex: ",replacement: "For example: $0",priority:0,options: "A"},
    {trigger: "obvious",replacement: "immediately obvious to the casual observer upon first inspection",priority:0,options: "A"},
    {trigger: "sorin ",replacement: "Sorin Jayaweera $0",priority:0,options: "A"},
    {trigger: "elliot ",replacement: "Elliot Bobrow $0",priority:0,options: "A"},
 {trigger: "jayden ",replacement: "Jayden Thadani $0",priority:0,options: "A"},
    
    
    // Math mode
	{trigger: "mk", replacement: "$$0$", options: "tA"},
	{trigger: "dm", replacement: "$$\n\\begin{align}\n$0\n\\end{align}\n$$", options: "tAw"},
	{trigger: "beg", replacement: "\\begin{$0}\n$1\n\\end{$0}", options: "mA"},
    
	// Dashes
	// {trigger: "--", replacement: "–", options: "tA"},
	// {trigger: "–-", replacement: "—", options: "tA"},
	// {trigger: "—-", replacement: "---", options: "tA"},


	// Greek letters
	{trigger: "@a", replacement: "\\alpha", options: "mA"},
	{trigger: "@A", replacement: "\\alpha", options: "mA"},
	{trigger: "@b", replacement: "\\beta", options: "mA"},
	{trigger: "@B", replacement: "\\beta", options: "mA"},
	{trigger: "@c", replacement: "\\chi", options: "mA"},
	{trigger: "@C", replacement: "\\chi", options: "mA"},
	{trigger: "@g", replacement: "\\gamma", options: "mA"},
	{trigger: "@G", replacement: "\\Gamma", options: "mA"},
	{trigger: "@d", replacement: "\\delta", options: "mA"},
	{trigger: "@D", replacement: "\\Delta", options: "mA"},
	{trigger: "@e", replacement: "\\epsilon", options: "mA"},
	{trigger: "@E", replacement: "\\epsilon", options: "mA"},
	{trigger: ":e", replacement: "\\varepsilon", options: "mA"},
	{trigger: ":E", replacement: "\\varepsilon", options: "mA"},
	{trigger: "@z", replacement: "\\zeta", options: "mA"},
	{trigger: "@Z", replacement: "\\zeta", options: "mA"},
	{trigger: "@t", replacement: "\\theta", options: "mA"},
	{trigger: "@T", replacement: "\\Theta", options: "mA"},
	{trigger: "@k", replacement: "\\kappa", options: "mA"},
	{trigger: "@K", replacement: "\\kappa", options: "mA"},
	{trigger: "@l", replacement: "\\lambda", options: "mA"},
	{trigger: "@L", replacement: "\\Lambda", options: "mA"},
	{trigger: "@m", replacement: "\\mu", options: "mA"},
	{trigger: "@M", replacement: "\\mu", options: "mA"},
	{trigger: "@r", replacement: "\\rho", options: "mA"},
	{trigger: "@R", replacement: "\\rho", options: "mA"},
	{trigger: "@s", replacement: "\\sigma", options: "mA"},
	{trigger: "@S", replacement: "\\Sigma", options: "mA"},
	{trigger: "ome", replacement: "\\omega", options: "mA"},
	{trigger: "@o", replacement: "\\omega", options: "mA"},
	{trigger: "@O", replacement: "\\Omega", options: "mA"},
	{trigger: "@u", replacement: "\\upsilon", options: "mA"},
	{trigger: "@U", replacement: "\\Upsilon", options: "mA"},
	{trigger: "([^\\\\])(${GREEK}|${SYMBOL})", replacement: "[[0]]\\[[1]]", options: "rmA", description: "Add backslash before greek letters and symbols"},
    

	// Insert space after greek letters and symbols, etc
    {trigger: "^",replacement: "^{$0}%1",priority:0,options: "mA"},
    
	{trigger: "\\\\(${GREEK}|${SYMBOL}|${SHORT_SYMBOL})([A-Za-z])", replacement: "\\[[0]] [[1]]", options: "rmA"},
	{trigger: "\\\\(${GREEK}|${SYMBOL}) sr", replacement: "\\[[0]]^{2}", options: "rmA"},
	{trigger: "\\\\(${GREEK}|${SYMBOL}) cb", replacement: "\\[[0]]^{3}", options: "rmA"},
	{trigger: "\\\\(${GREEK}|${SYMBOL}) rd", replacement: "\\[[0]]^{$0}$1", options: "rmA"},
	{trigger: "\\\\(${GREEK}|${SYMBOL}) hat", replacement: "\\hat{\\[[0]]}", options: "rmA"},
	{trigger: "\\\\(${GREEK}|${SYMBOL}) dot", replacement: "\\dot{\\[[0]]}", options: "rmA"},
	{trigger: "\\\\(${GREEK}|${SYMBOL}) bar", replacement: "\\bar{\\[[0]]}", options: "rmA"},
	{trigger: "\\\\(${GREEK}|${SYMBOL}) vec", replacement: "\\vec{\\[[0]]}", options: "rmA"},
	{trigger: "\\\\(${GREEK}|${SYMBOL}) tilde", replacement: "\\tilde{\\[[0]]}", options: "rmA"},
	{trigger: "\\\\(${GREEK}|${SYMBOL}) und", replacement: "\\underline{\\[[0]]}", options: "rmA"},
	{trigger: "\\\\(${GREEK}),\\.", replacement: "\\boldsymbol{\\[[0]]}", options: "rmA"},
	{trigger: "\\\\(${GREEK})\\.,", replacement: "\\boldsymbol{\\[[0]]}", options: "rmA"},


	// Operations
	{trigger: "te", replacement: "\\text{ $0 }$1", options: "m"},
	{trigger: "text", replacement: "\\text{$0}$1", options: "mA"},
	{trigger: "bf", replacement: "\\mathbf{$0}", options: "mA"},
	{trigger: "sr", replacement: "^{2}", options: "mA"},
	{trigger: "cb", replacement: "^{3}", options: "mA"},
	{trigger: "rd", replacement: "^{$0}$1", options: "mA"},
	{trigger: "_", replacement: "_{$0}$1", options: "mA"},
	{trigger: "sts", replacement: "_\\text{$0}", options: "rmA"},
	{trigger: "sq", replacement: "\\sqrt{ $0 }$1", options: "mA"},
	{trigger: "//", replacement: "\\frac{$0}{$1}$2", options: "mA"},
	{trigger: "ee", replacement: "e^{ $0 }$1", options: "mA"},
    
    {trigger: "cal", replacement: "\\mathcal{$0} $1", options: "mA"},
	{trigger: "rm", replacement: "\\mathrm{$0}$1", options: "mA"},
	{trigger: "conj", replacement: "^{*}", options: "mA"},
	{trigger: "trace", replacement: "\\mathrm{Tr}", options: "mA"},
	{trigger: "det", replacement: "\\det{($0)} $1", options: "mA"},
	{trigger: "re", replacement: "\\mathrm{Re}", options: "mA"},
	{trigger: "im", replacement: "\\mathrm{Im}", options: "mA"},

	{trigger: "([a-zA-Z]),\\.", replacement: "\\mathbf{[[0]]}", options: "rmA"},
	{trigger: "([a-zA-Z])\\.,", replacement: "\\mathbf{[[0]]}", options: "rmA"},
	{trigger: "([A-Za-z])(\\d)", replacement: "[[0]]_{[[1]]}", options: "rmA", description: "Auto letter subscript", priority: -1},
	{trigger: "([A-Za-z])_(\\d\\d)", replacement: "[[0]]_{[[1]]}", options: "rmA"},
	{trigger: "\\hat{([A-Za-z])}(\\d)", replacement: "hat{[[0]]}_{[[1]]}", options: "rmA"},
	{trigger: "\\\\mathbf{([A-Za-z])}(\\d)", replacement: "\\mathbf{[[0]]}_{[[1]]}", options: "rmA"},
	{trigger: "\\\\vec{([A-Za-z])}(\\d)", replacement: "\\vec{[[0]]}_{[[1]]}", options: "rmA"},
	{trigger: "([a-zA-Z])bar", replacement: "\\bar{[[0]]}", options: "rmA"},
	{trigger: "([a-zA-Z])hat", replacement: "\\hat{[[0]]}", options: "rmA"},
	{trigger: "([a-zA-Z])ddot", replacement: "\\ddot{[[0]]}", options: "rmA", priority: 3},
	{trigger: "([a-zA-Z])dot", replacement: "\\dot{[[0]]}", options: "rmA", priority: 1},
	{trigger: "([a-zA-Z])vec", replacement: "\\vec{[[0]]}", options: "rmA"},
	{trigger: "([a-zA-Z])tilde", replacement: "\\tilde{[[0]]}", options: "rmA"},
	{trigger: "([a-zA-Z])und", replacement: "\\underline{[[0]]}", options: "rmA"},
	{trigger: "bar", replacement: "\\bar{$0}$1", options: "mA"},
	{trigger: "hat", replacement: "\\hat{$0}$1", options: "mA"},
	{trigger: "dot", replacement: "\\dot{$0}$1", options: "mA"},
	{trigger: "ddot", replacement: "\\ddot{$0}$1", options: "mA", priority: 2},
    {trigger: "hdot", replacement: "\\circ \ $0", options: "mA", priority: 1},
    {trigger: "hdt", replacement: "\\circ \ $0", options: "mA", priority: 1},
    {trigger: "circ", replacement: "\\circ \ $0", options: "mA", priority: 1},
	{trigger: "cdot", replacement: "\\cdot", options: "mA", priority: 2},
	{trigger: "vec", replacement: "\\vec{$0}$1", options: "mA"},
	{trigger: "tilde", replacement: "\\tilde{$0}$1", options: "mA"},
	{trigger: "und", replacement: "\\underline{$0}$1", options: "mA"},

	{trigger: "([^\\\\])(arcsin|arccos|arctan|arccot|arccsc|arcsec|sin|cos|tan|cot|csc|sec)", replacement: "[[0]]\\[[1]]", options: "rmA"},
	{trigger: "\\\\(arcsin|arccos|arctan|arccot|arccsc|arcsec|sin|cos|tan|cot|csc|sec)([A-Za-gi-z])", replacement: "\\[[0]] [[1]]", options: "rmA"}, // Insert space after trig funcs. Skips letter "h" to allow sinh, cosh, etc.
	{trigger: "\\\\(arcsinh|arccosh|arctanh|arccoth|arcsch|arcsech|sinh|cosh|tanh|coth|csch|sech)([A-Za-z])", replacement: "\\[[0]] [[1]]", options: "rmA"}, // Insert space after trig funcs
	{trigger: "\\\\(neq|geq|leq|gg|ll|sim)([0-9]+)", replacement: "\\[[0]] [[1]]", options: "rmA"}, // Insert space after inequality symbols


	// Visual operations
	{trigger: "U", replacement: "\\underbrace{ ${VISUAL} }_{ $0 }", options: "mA"},
	{trigger: "B", replacement: "\\underset{ $0 }{ ${VISUAL} }", options: "mA"},
	{trigger: "C", replacement: "\\cancel{ ${VISUAL} }", options: "mA"},
	{trigger: "K", replacement: "\\cancelto{ $0 }{ ${VISUAL} }", options: "mA"},
	{trigger: "S", replacement: "\\sqrt{ ${VISUAL} }", options: "mA"},


	// Symbols
	{trigger: "ooo", replacement: "\\infty", options: "mA"},
	{trigger: "sum", replacement: "\\sum", options: "mA"},
	{trigger: "prod", replacement: "\\prod", options: "mA"},
	{trigger: "lim", replacement: "\\lim_{ ${0:n} \\to ${1:\\infty} } $2", options: "mA"},
	{trigger: "([^\\\\])pm", replacement: "[[0]]\\pm", options: "rm"},
	{trigger: "([^\\\\])mp", replacement: "[[0]]\\mp", options: "rm"},
	{trigger: "+-", replacement: "\\pm", options: "mA"},
	{trigger: "-+", replacement: "\\mp", options: "mA"},
	{trigger: "...", replacement: "\\dots", options: "mA"},
	{trigger: "v...", replacement: "\\vdots", options: "mA"},
	{trigger: "vdts", replacement: "\\vdots", options: "m"},
	{trigger: "ddts", replacement: "\\ddots", options: "m"},
	{trigger: "<->", replacement: "\\leftrightarrow ", options: "mA"},
	{trigger: "->", replacement: "\\to  $0", options: "mA"},
	{trigger: "!>", replacement: "\\mapsto", options: "mA"},
	{trigger: "invs", replacement: "^{-1}", options: "mA"},
	{trigger: "\\\\\\", replacement: "\\setminus", options: "mA"},
	{trigger: "||", replacement: "\\mid", options: "mA"},
	{trigger: "and", replacement: "\\cap", options: "mA"},
	{trigger: "orr", replacement: "\\cup", options: "mA"},
	{trigger: "inn", replacement: "\\in", options: "mA"},
	{trigger: "notin", replacement: "\\not\\in", options: "mA"},
	{trigger: "\\subset eq", replacement: "\\subseteq", options: "mA"},
	{trigger: "eset", replacement: "\\emptyset", options: "mA"},
	{trigger: "set", replacement: "\\left\\{ $0 \\right\\}$1", options: "mA"},
	{trigger: "=>", replacement: "\\implies", options: "mA"},
	{trigger: "=<", replacement: "\\impliedby", options: "mA"},
	{trigger: "iff", replacement: "\\iff", options: "mA"},
	{trigger: "e\\xi sts", replacement: "\\exists", options: "mA", priority: 1},
	{trigger: "===", replacement: "\\equiv", options: "mA"},
	{trigger: "Sq", replacement: "\\square", options: "mA"},
	{trigger: "!=", replacement: "\\neq", options: "mA"},
	{trigger: ">=", replacement: "\\geq", options: "mA"},
	{trigger: "<=", replacement: "\\leq", options: "mA"},
	{trigger: ">>", replacement: "\\gg", options: "mA"},
	{trigger: "<<", replacement: "\\ll", options: "mA"},
	{trigger: "~~", replacement: "\\sim", options: "mA"},
	{trigger: "\\sim ~", replacement: "\\approx", options: "mA"},
	{trigger: "prop", replacement: "\\propto", options: "mA"},
	{trigger: "nabl", replacement: "\\nabla", options: "mA"},
	{trigger: "del", replacement: "\\nabla", options: "mA"},
	{trigger: "xx", replacement: "\\times  $0", options: "m"},
    {trigger: "\\vec{x}x", replacement: "\\times  $0", options: "mA"},
    
	{trigger: "**", replacement: "\\cdot", options: "mA"},
	{trigger: "para", replacement: "\\parallel", options: "mA"},

	{trigger: "xnn", replacement: "x_{n}", options: "mA"},
	{trigger: "xii", replacement: "x_{i}", options: "mA"},
	{trigger: "xjj", replacement: "x_{j}", options: "mA"},
	{trigger: "xp1", replacement: "x_{n+1}", options: "mA"},
	{trigger: "ynn", replacement: "y_{n}", options: "mA"},
	{trigger: "yii", replacement: "y_{i}", options: "mA"},
	{trigger: "yjj", replacement: "y_{j}", options: "mA"},

	{trigger: "mcal", replacement: "\\mathcal{$0}$1", options: "mA"},
	{trigger: "mbb", replacement: "\\mathbb{$0}$1", options: "mA"},
	{trigger: "ell", replacement: "\\ell", options: "mA"},
	{trigger: "lll", replacement: "\\ell", options: "mA"},
	{trigger: "LL", replacement: "\\mathcal{L}", options: "mA"},
	{trigger: "HH", replacement: "\\mathcal{H}", options: "mA"},
	{trigger: "CC", replacement: "\\mathbb{C}", options: "mA"},
	{trigger: "RR", replacement: "\\mathbb{R}^{$0}$1", options: "mA"},
    
	{trigger: "PP", replacement: "\\mathscr{P}_{$0} $1", options: "mA"},
    
	{trigger: "ZZ", replacement: "\\mathbb{Z}", options: "mA"},
	{trigger: "NN", replacement: "\\mathbb{N}", options: "mA"},
	{trigger: "II", replacement: "\\mathbb{1}", options: "mA"},
	{trigger: "\\mathbb{1}I", replacement: "\\hat{\\mathbb{1}}", options: "mA"},
	{trigger: "AA", replacement: "\\mathcal{A}", options: "mA"},
	{trigger: "BB", replacement: "\\mathbf{B}", options: "mA"},
	{trigger: "EE", replacement: "\\mathbf{E}", options: "mA"},


	// Unit vectors
	{trigger: ":i", replacement: "\\mathbf{i}", options: "mA"},
	{trigger: ":j", replacement: "\\mathbf{j}", options: "mA"},
	{trigger: ":k", replacement: "\\mathbf{k}", options: "mA"},
	{trigger: ":x", replacement: "\\hat{\\mathbf{x}}", options: "mA"},
	{trigger: ":y", replacement: "\\hat{\\mathbf{y}}", options: "mA"},
	{trigger: ":z", replacement: "\\hat{\\mathbf{z}}", options: "mA"},


	// Derivatives
    {trigger: "der", replacement: "\\frac{ d ${0:y} }{d ${1:x} } $2", options: "mA"},
	{trigger: "par", replacement: "\\frac{ \\partial ${0:y} }{ \\partial ${1:x} } $2", options: "mA"},
	{trigger: "pa2", replacement: "\\frac{ \\partial^{2} ${0:y} }{ \\partial ${1:x}^{2} } $2", options: "mA"},
	{trigger: "pa3", replacement: "\\frac{ \\partial^{3} ${0:y} }{ \\partial ${1:x}^{3} } $2", options: "mA"},
	{trigger: "pa([A-Za-z])([A-Za-z])", replacement: "\\frac{ \\partial [[0]] }{ \\partial [[1]] } ", options: "rm"},
	{trigger: "pa([A-Za-z])([A-Za-z])([A-Za-z])", replacement: "\\frac{ \\partial^{2} [[0]] }{ \\partial [[1]] \\partial [[2]] } ", options: "rm"},
	{trigger: "pa([A-Za-z])([A-Za-z])2", replacement: "\\frac{ \\partial^{2} [[0]] }{ \\partial [[1]]^{2} } ", options: "rmA"},
	{trigger: "de([A-Za-z])([A-Za-z])", replacement: "\\frac{ d[[0]] }{ d[[1]] } ", options: "rm"},
	{trigger: "de([A-Za-z])([A-Za-z])2", replacement: "\\frac{ d^{2}[[0]] }{ d[[1]]^{2} } ", options: "rmA"},
	{trigger: "ddt", replacement: "\\frac{d}{dt} ", options: "m"},
	{trigger: "ddx", replacement: "\\frac{d}{dx} ", options: "m"},
	{trigger: "ddy", replacement: "\\frac{d}{dy} ", options: "m"},


	// Integrals
	{trigger: "oinf", replacement: "\\int_{0}^{\\infty} $0 \\, d${1:x} $2", options: "mA"},
	{trigger: "infi", replacement: "\\int_{-\\infty}^{\\infty} $0 \\, d${1:x} $2", options: "mA"},
	{trigger: "dint", replacement: "\\int_{${0:0}}^{${1:\\infty}} $2 \\, d${3:x} $4", options: "mA"},
	{trigger: "oint", replacement: "\\oint", options: "mA"},
	{trigger: "iiint", replacement: "\\iiint", options: "mA"},
	{trigger: "iint", replacement: "\\iint", options: "mA"},
	{trigger: "int", replacement: "\\int $0 \\, d${1:x} $2", options: "mA"},


	// Physics
	{trigger: "kbt", replacement: "k_{B}T", options: "mA"},


	// Quantum mechanics
	{trigger: "hba", replacement: "\\hbar", options: "mA"},
	{trigger: "dag", replacement: "^{\\dagger}", options: "mA"},
	{trigger: "o+", replacement: "\\oplus ", options: "mA"},
	{trigger: "ox", replacement: "\\otimes ", options: "mA"},
	{trigger: "ot\\mathrm{Im}es", replacement: "\\otimes ", options: "mA"}, // Handle conflict with "im" snippet
	{trigger: "bra", replacement: "\\bra{$0} $1", options: "mA"},
	{trigger: "ket", replacement: "\\ket{$0} $1", options: "mA"},
	{trigger: "brk", replacement: "\\braket{ $0 | $1 } $2", options: "mA"},
	{trigger: "\\\\bra{([^|]+)\\|", replacement: "\\braket{ [[0]] | $0 ", options: "rmA", description: "Convert bra into braket"},
	{trigger: "\\\\bra{(.+)}([^ ]+)>", replacement: "\\braket{ [[0]] | $0 ", options: "rmA", description: "Convert bra into braket (alternate)"},
	{trigger: "outp", replacement: "\\ket{${0:\\psi}} \\bra{${0:\\psi}} $1", options: "mA"},


	// Chemistry
	{trigger: "pu", replacement: "\\pu{ $0 }", options: "mA"},
	{trigger: "msun", replacement: "M_{\\odot}", options: "mA"},
	{trigger: "solm", replacement: "M_{\\odot}", options: "mA"},
	{trigger: "cee", replacement: "\\ce{ $0 }", options: "mA"},
	{trigger: "iso", replacement: "{}^{${0:4}}_{${1:2}}${2:He}", options: "mA"},
	{trigger: "hel4", replacement: "{}^{4}_{2}He ", options: "mA"},
	{trigger: "hel3", replacement: "{}^{3}_{2}He ", options: "mA"},


	// Environments
	{trigger: "pmat", replacement: "\\begin{pmatrix}\n$0\n\\end{pmatrix}", options: "mA"},
	{trigger: "bmat", replacement: "\\begin{bmatrix}\n$0\n\\end{bmatrix}", options: "mA"},
	{trigger: "Bmat", replacement: "\\begin{Bmatrix}\n$0\n\\end{Bmatrix}", options: "mA"},
	{trigger: "vmat", replacement: "\\begin{vmatrix}\n$0\n\\end{vmatrix}", options: "mA"},
	{trigger: "Vmat", replacement: "\\begin{Vmatrix}\n$0\n\\end{Vmatrix}", options: "mA"},
	{trigger: "case", replacement: "\\begin{cases}\n$0\n\\end{cases}", options: "mA"},
	{trigger: "align", replacement: "\\begin{align}\n$0\n\\end{align}", options: "mA"},
	{trigger: "array", replacement: "\\begin{array}\n$0\n\\end{array}", options: "mA"},
	{trigger: "matrix", replacement: "\\begin{matrix}\n$0\n\\end{matrix}", options: "mA"},


	// Brackets
	{trigger: "avg", replacement: "\\langle $0 \\rangle $1", options: "mA"},
	{trigger: "norm", replacement: "\\lvert $0 \\rvert $1", options: "mA", priority: 1},
	{trigger: "ceil", replacement: "\\lceil $0 \\rceil $1", options: "mA"},
	{trigger: "floor", replacement: "\\lfloor $0 \\rfloor $1", options: "mA"},
	{trigger: "mod", replacement: "|$0|$1", options: "mA"},
	{trigger: "(", replacement: "(${VISUAL})", options: "mA"},
	{trigger: "[", replacement: "[${VISUAL}]", options: "mA"},
	{trigger: "{", replacement: "{${VISUAL}}", options: "mA"},
	{trigger: "(", replacement: "($0)$1", options: "mA"},
	{trigger: "{", replacement: "{$0}$1", options: "mA"},
	{trigger: "[", replacement: "[$0]$1", options: "mA"},
	{trigger: "lr(", replacement: "\\left( $0 \\right) $1", options: "mA"},
	{trigger: "lr|", replacement: "\\left| $0 \\right| $1", options: "mA"},
	{trigger: "lr{", replacement: "\\left\\{ $0 \\right\\} $1", options: "mA"},
	{trigger: "lr[", replacement: "\\left[ $0 \\right] $1", options: "mA"},
	{trigger: "lra", replacement: "\\left< $0 \\right> $1", options: "mA"},


	// Misc
	{trigger: "tayl", replacement: "${0:f}(${1:x} + ${2:h}) = ${0:f}(${1:x}) + ${0:f}'(${1:x})${2:h} + ${0:f}''(${1:x}) \\frac{${2:h}^{2}}{2!} + \\dots$3", options: "mA"},
	{trigger: /iden(\d)/, replacement: (match) => {
		const n = match[1];

		let arr = [];
		for (let j = 0; j < n; j++) {
			arr[j] = [];
			for (let i = 0; i < n; i++) {
				arr[j][i] = (i === j) ? 1 : 0;
			}
		}

		let output = arr.map(el => el.join(" & ")).join(" \\\\\n");
		output = `\\begin{pmatrix}\n${output}\n\\end{pmatrix}`;
		return output;
	}, options: "mA", description: "N x N identity matrix"},
]
