# Belajar Goroutine di Golang

## Daftar Materi
- Pendahuluan
- Pengenalan Concurrency dan Parallel Programming
- Pengenalan Goroutine
- Membuat Project
- Membuat Goroutine
- Goroutine Sangat Ringan
- Pengenalan Channel
- Membuat Channel
- Channel Sebagai Parameter
- Channel In dan Out
- Buffered Channel
- Range Channel
- Select Channel
- Default Select
- Race Condition
- sync.Mutex
- sync.RWMutex
- Deadlock
- sync.WaitGroup
- sync.Once
- sync.Pool
- sync.Map
- sync.Cond
- Atomic
- time.Timer
- time.Ticker
- GOMAXPROCS

---

## Ringkasan Materi

### Concurrency & Parallel Programming
Konsep dasar perbedaan concurrency dan parallelism, serta kenapa penting dalam aplikasi modern.

### Goroutine
Penjelasan apa itu goroutine, cara kerja, dan keunggulannya dibanding thread biasa.  
Contoh sederhana:
```go
package main

import (
    "fmt"
    "time"
)

func sayHello() {
    fmt.Println("Hello dari Goroutine!")
}

func main() {
    go sayHello()
    time.Sleep(time.Second) // tunggu goroutine selesai
}
