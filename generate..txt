    def validate_quote_input(self):
        """Проверка корректности ввода новой цитаты"""
        text = self.text_entry.get().strip()
        author = self.author_entry.get().strip()
        topic = self.topic_entry.get().strip()

        if not text:
            messagebox.showerror("Ошибка", "Текст цитаты не может быть пустым")
            return False
        if not author:
            messagebox.showerror("Ошибка", "Автор не может быть пустым")
            return False
        if not topic:
            messagebox.showerror("Ошибка", "Тема не может быть пустой")
            return False

        return True, text, author, topic