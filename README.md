# COP2664-1-Lesson-8-Programming-Assignment-Counter-App
This is a GitHub repository link for the Xcode Programming Assignment from Module 8.

// This program is created to build a counter app using SwiftUI framework in Swift language. It allows the user to increment, decrement, and reset the counter value via the buttons provided.

import SwiftUI

struct ContentView: View {
    @State private var count = 0
    // @State is a property wrapper that allows the view to store and manage its own state.

    var body: some View {
        VStack(spacing: 20) {
            Text("Count: \(count)")
                .font(.largeTitle)
                .bold()
            // This line displays the current count value.

            HStack(spacing: 20) {
                Button(action: {
                    count -= 1
                }) {
                    Text("Decrement")
                        .padding()
                        .frame(minWidth: 100)
                        .background(Color.red)
                        .foregroundColor(.white)
                        .cornerRadius(10)
                }
                // This button decrements the count value by 1 when pressed.

                Button(action: {
                    count = 0
                }) {
                    Text("Reset")
                        .padding()
                        .frame(minWidth: 100)
                        .background(Color.yellow)
                        .foregroundColor(.white)
                        .cornerRadius(10)
                }
                // This button resets the count value to 0 when pressed.

                Button(action: {
                    count += 1
                }) {
                    Text("Increment")
                        .padding()
                        .frame(minWidth: 100)
                        .background(Color.green)
                        .foregroundColor(.white)
                        .cornerRadius(10) // This button increments the count value by 1 when pressed.
                }
            }
        }
        .padding() // This line adds padding to the VStack.
    }
}
