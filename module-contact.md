# Mammoth Contact Module

    namespace Example;
    use Mammoth\Contact;

	class ContactController {
		public function contact() {
			$contactFrom = new Contact\Form();
			if ($contactFrom->process()) {
				return;
			}
			$this->render('contact');
		}
	}

