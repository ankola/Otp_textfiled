# Otp_textfiled
One textfield to another textfield auto redirect


//MARK:- ------ UITextField Delegate ---------
    func textField(_ textField: UITextField, shouldChangeCharactersIn range: NSRange, replacementString string: String) -> Bool {
        
        let str : String = string.trimmingCharacters(in: .whitespaces)

        if str.count == 1 && textField == txt1 {
            textField.text = str
            self.txt2.becomeFirstResponder()
            return true
            
        } else if str.count == 1 && textField == txt2 {
            textField.text = str
            self.txt3.becomeFirstResponder()
            return true
            
        } else if str.count == 1 && textField == txt3 {
            textField.text = str
            self.txt4.becomeFirstResponder()
            return true
            
        } else if str.count == 1 && textField == txt4 {
            textField.text = str
            self.txt5.becomeFirstResponder()
            return true
            
        } else if str.count == 1 && textField == txt5 {
            textField.text = str
            self.txt6.becomeFirstResponder()
            return true
            
        } else if str.count == 1 && textField == txt6 {
            textField.text = str
            self.txt6.resignFirstResponder()
            return true
            
        } else if textField.text?.count == 1 && string.count == 0 && textField == txt6 {
            textField.text = str
            self.txt5.becomeFirstResponder()
            return false
            
        } else if textField.text?.count == 1 && string.count == 0 && textField == txt5 {
            textField.text = str
            self.txt4.becomeFirstResponder()
            return false
            
        } else if textField.text?.count == 1 && string.count == 0 && textField == txt4 {
            textField.text = str
            self.txt3.becomeFirstResponder()
            return false
            
        } else if textField.text?.count == 1 && string.count == 0 && textField == txt3 {
            textField.text = str
            self.txt2.becomeFirstResponder()
            return false
            
        } else if textField.text?.count == 1 && string.count == 0 && textField == txt2 {
            textField.text = str
            self.txt1.becomeFirstResponder()
            return false
            
        } else if textField.text?.count == 1 && string.count == 0 && textField == txt1 {
            textField.text = str
            self.txt1.resignFirstResponder()
            return false
            
        } else {
            return false
        }
    }
