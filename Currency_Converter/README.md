# React + Vite

This template provides a minimal setup to get React working in Vite with HMR and some ESLint rules.

Currently, two official plugins are available:

- [@vitejs/plugin-react](https://github.com/vitejs/vite-plugin-react/blob/main/packages/plugin-react/README.md) uses [Babel](https://babeljs.io/) for Fast Refresh
- [@vitejs/plugin-react-swc](https://github.com/vitejs/vite-plugin-react-swc) uses [SWC](https://swc.rs/) for Fast Refresh

## Expanding the ESLint configuration

If you are developing a production application, we recommend using TypeScript and enable type-aware lint rules. Check out the [TS template](https://github.com/vitejs/vite/tree/main/packages/create-vite/template-react-ts) to integrate TypeScript and [`typescript-eslint`](https://typescript-eslint.io) in your project.


<!-- BGChangerCode  -->

<!-- import { useState } from 'react'


function App() {
  const [color, setColor] = useState("black")


  return (
    <>
      <div className='w-full h-screen duration-200' style={{ backgroundColor: color }}>

        <div className='fixed flex flex-wrap justify-center top-12 inset-x-0 px-2 border-1'>
          <div className='flex flex-wrap justify-center gap-3 shadow-lg bg-white px-3 py-2 rounded-3xl'>
            <button onClick={()=> setColor("red")} className="outline-none px-4 py-1 rounded-full text-white shadow-lg"
              style={{ backgroundColor: "red" }}
            >Red</button>
            <button onClick={()=> setColor("green")}
             className="outline-none px-4 py-1 rounded-full text-white shadow-lg"
              style={{ backgroundColor: "green" }}
            >Green</button>
            <button onClick={()=> setColor("blue")}
             className="outline-none px-4 py-1 rounded-full text-white shadow-lg"
              style={{ backgroundColor: "blue" }}
            >Blue</button>
            <button onClick={()=> setColor("Olive")} className="outline-none px-4 py-1 rounded-full text-white shadow-lg"
              style={{ backgroundColor: "Olive" }}
            >Olive</button>
            <button onClick={()=> setColor("grey ")} className="outline-none px-4 py-1 rounded-full text-white shadow-lg"
              style={{ backgroundColor: "grey " }}
            >Grey</button>
            <button onClick={()=> setColor("Yellow")} className="outline-none px-4 py-1 rounded-full text-black shadow-lg"
              style={{ backgroundColor: "Yellow" }}
            >Yellow</button>
            <button onClick={()=> setColor("Pink")} className="outline-none px-4 py-1 rounded-full text-black shadow-lg"
              style={{ backgroundColor: "Pink" }}
            >Pink</button>
            <button onClick={()=> setColor("Purple")} className="outline-none px-4 py-1 rounded-full text-black shadow-lg"
              style={{ backgroundColor: "Purple" }}
            >Purple</button>
            <button onClick={()=> setColor("Lavender")} className="outline-none px-4 py-1 rounded-full text-black shadow-lg"
              style={{ backgroundColor: "Lavender" }}
            >Lavender</button>
             <button onClick={()=> setColor("White")} className="outline-none px-4 py-1 rounded-full text-black shadow-lg"
              style={{ backgroundColor: "White" }}
            >White</button>
             <button onClick={()=> setColor("Black")} className="outline-none px-4 py-1 rounded-full text-white shadow-lg"
              style={{ backgroundColor: "Black" }}
            >Black</button>
          </div>
        </div>

      </div>

    </>
  )
}

export default App -->


<!-- PASSWORD GENERATOR CODE 
function App() {
  const [length, setLength] = useState(8)
  const [numberAllowed, setNumberallowed] = useState(false)
  const [charAllowed, setCharAllowed] = useState(false)
  const [password, setpassword] = useState("")

  const passwordRef = useRef(null)

  const passwordGenerator = useCallback(() => {
    let pass = ""
    let str = "ABCDEFGHIJKLMNOPQRSTUVWXYZabcdefghijklmnopqrstuvwxyz"
    if (numberAllowed) str += "0123456789"
    if (charAllowed) str += "!@#$%^&*-_+=[]{}~`"
    for (let i = 0; i < length; i++) {
      let char = Math.floor(Math.random() * str.length + 1)
      pass += str.charAt(char)
    setpassword(pass)

    }

  }, [length, numberAllowed, charAllowed, setpassword])

  const copyPasswordToClipboard = useCallback( ()=>{
    passwordRef.current?.select()
    passwordRef.current?.setSelectionRange(0,199)
    window.navigator.clipboard.writeText(password)
  },[password])


  useEffect(() => {
    passwordGenerator()
  }, [length, numberAllowed, charAllowed, passwordGenerator])



  return (
    <>
      <div className="w-full max-w-md mx-auto shadow-md rounded-lg px-4 py-3 my-8 bg-gray-800 text-orange-500">
        <h1 className='text-white text-center my-3'>Password Generator</h1>
        <div className="flex shadow rounded-lg overflow-hidden mb-4">
          <input
            type="text"
            value={password}
            className="outline-none w-full py-1 px-3"
            placeholder="Password"
            readOnly
            ref={passwordRef}
          />
          <button onClick={copyPasswordToClipboard}
          className='outline-none bg-blue-700 text-white px-3 py-0.5 shrink-0'>copy</button>

        </div>
        <div className='flex text-sm gap-x-2'>
          <div className='flex items-center gap-x-1'>
            <input
              type="range"
              min={6}
              max={100}
              value={length}
              className='cursor-pointer'
              onChange={(e) => { setLength(e.target.value) }}
            />
            <label>Length:-{length}</label>
          </div>

          <div className="flex items-center gap-x-1">
            <input
              type="checkbox"
              defaultChecked={numberAllowed}
              id='numberInput'
              onChange={() => {
                setNumberallowed((prev) => !prev)
              }}
            />
            <label htmlFor="numberInput">Numbers</label>

          </div>
          <div className="flex items-center gap-x-1">
            <input
              type="checkbox"
              defaultChecked={charAllowed}
              id="characterInput"
              onChange={() => {
                setCharAllowed((prev) => !prev)
              }}
            />
            <label htmlFor="characterInput">Characters</label>

          </div>

        </div>

      </div>

    </>
  )
}

export default App -->