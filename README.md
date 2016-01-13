# Guessing-Game-IOS-Swift-2-
This is an IOS based game (Swift 2 platform) that asks user(s) to guess the number of finger(s) one is holding up.
It uses a random function generator to generate a number at random between 1-5 and the asks user for an input.
If the user guesses it correctly, a message is displayed showing the correct number of fingers. If not, he/she is given a choice of trying it out again.

//  ViewController.swift
//  Guessing game
//  Created by Aditya Kaul on 14/01/16.
//  Copyright © 2016 Occultus. All rights reserved.


import UIKit

class ViewController: UIViewController {

    @IBOutlet var label1: UILabel!
    @IBOutlet var textField1: UITextField!
    var anti = Int(arc4random_uniform(5) + 1)
    @IBAction func button1(sender: AnyObject) {
        
        if textField1.text == String(anti) {
            label1.text = "You guessed it right. I was holding \(textField1.text!) fingers"
        } else {
            label1.text = "Icorrect guess. Try again."
        }
        
    }
    override func viewDidLoad() {
        super.viewDidLoad()
        // Do any additional setup after loading the view, typically from a nib.
    }

    override func didReceiveMemoryWarning() {
        super.didReceiveMemoryWarning()
        // Dispose of any resources that can be recreated.
    }
    
}
