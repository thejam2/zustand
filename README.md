# zustand

## 설치
```
npm install zustand
# Or, use any package manager of your choice.
```

## 기본 사용 방법
```
import { create } from 'zustand'

//store 생성
const useStore = create((set) => ({
  bears: 0,
  increasePopulation: () => set((state) => ({ bears: state.bears + 1 })),
  removeAllBears: () => set({ bears: 0 }),
}))

//사용
function BearCounter() {
  const bears = useStore((state) => state.bears)
  return <h1>{bears} around here...</h1>
}
function Controls() {
  const increasePopulation = useStore((state) => state.increasePopulation)
  return <button onClick={increasePopulation}>one up</button>
}
```
