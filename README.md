# QA-Chatbot-Turkish
TR:
--------------------------------------------------------------
Proje Açıklaması
Bu proje, Türkçe dilinde soru-cevap (QA) chatbot geliştirmek amacıyla çeşitli doğal dil işleme (NLP) araçlarını kullanmaktadır. Projenin temel amacı, kullanıcıların sordukları sorulara uygun ve doğru cevaplar vermek için metinleri anlamak ve işlemek üzerine odaklanmaktadır. Aşağıda, projede kullanılan ana araçlar ve kitaplıkların detaylı açıklamaları verilmiştir:

Kullanılan Araçlar ve Kitaplıklar
Sentence-Transformers:
Sentence-Transformers, metin verilerini yüksek boyutlu gömme (embedding) vektörlerine dönüştüren bir araçtır. Bu vektörler, metinlerin anlamlarını sayısal bir biçimde temsil eder. Projede, kullanıcıların sorduğu soruların metin temsillerini elde etmek ve bu temsiller üzerinden benzerlik aramaları gerçekleştirmek için kullanılmıştır. Sentence-Transformers, çeşitli önceden eğitilmiş modeller sunarak farklı diller ve metin türleri için gömme vektörleri oluşturmayı mümkün kılar. Bu sayede, projemizde Türkçe dilinde verimli ve etkili bir şekilde metin temsilleri oluşturulabilmiştir.

AutoTokenizer:
AutoTokenizer, metinleri belirli bir dil modeli için tokenlere dönüştüren bir araçtır. Tokenler, metinlerin daha küçük anlamlı parçalara bölünmüş halleridir. Bu işlem, metinleri dil modelinin anlayabileceği bir biçime dönüştürerek, modelin metni işlemeye başlamadan önce hazırlık yapmasını sağlar. Örneğin, "Merhaba, nasılsın?" cümlesi, tokenizer tarafından ['Merhaba', ',', 'nasılsın', '?'] gibi parçalarına ayrılabilir. Bu adım, modelin metni doğru bir şekilde anlaması ve işlem yapması için kritik öneme sahiptir.

KeyBERT:
KeyBERT, metinlerden anlamlı anahtar kelimeler ve terimler çıkarmak için kullanılan bir araçtır. Bu işlem, metnin ana konularını belirlemek ve öne çıkan kelimeleri vurgulamak için kullanılır. KeyBERT, metinlerin içerdiği en önemli kelimeleri ve ifadeleri bulmak için BERT tabanlı bir yaklaşıma dayanır. Bu sayede, projemizde kullanıcıların sorduğu soruların temel konularını anlamak ve bu konulara uygun cevaplar önerme süreçlerinde kullanılmıştır. Örneğin, bir paragraftan "yapay zeka", "makine öğrenmesi" gibi anahtar kelimeler çıkarılarak, bu kelimelere yönelik daha spesifik cevaplar sunulabilir.

FAISS (Facebook AI Similarity Search):
FAISS, yüksek boyutlu vektörleri hızlı ve verimli bir şekilde aramak için kullanılan bir araçtır. Yüksek boyutlu vektörler, genellikle metinlerin gömme temsilleridir ve bu temsiller üzerinden benzerlik aramaları gerçekleştirilir. FAISS, büyük veri setleri üzerinde hızlı bir şekilde en yakın komşu araması (nearest neighbor search) yapma imkanı tanır. Bu projede, kullanıcının sorduğu sorunun vektör temsili ile daha önce cevaplandırılmış soruların vektör temsilleri arasında benzerlik araması yaparak en uygun cevapları bulmak için kullanılmıştır. FAISS, hem doğruluk hem de hız açısından verimli arama sonuçları elde etmemize imkan tanır, bu da kullanıcılara hızlı ve doğru cevaplar sunmayı mümkün kılar.


EN:
--------------------------------------------------------------
Project Description
This project is focused on developing a question-answering (QA) chatbot in Turkish using various natural language processing (NLP) tools. The main goal of the project is to understand and process text to provide appropriate and accurate responses to user queries. Below is a detailed description of the key tools and libraries used in this project:

Tools and Libraries Used
Sentence-Transformers:
Sentence-Transformers is a tool used to convert text data into high-dimensional embedding vectors. These vectors provide numerical representations of the text, which are used for similarity searches. In this project, Sentence-Transformers is employed to obtain text representations of user queries, which are then used to perform similarity searches. The tool offers various pre-trained models that allow for the creation of embeddings suitable for different languages and text types. This enables efficient and effective text representation for Turkish in our project.

AutoTokenizer:
AutoTokenizer is used to tokenize text for a specific language model. Tokenization breaks down text into smaller, meaningful units called tokens. This process transforms the text into a format that the model can understand, ensuring accurate processing. For example, the sentence "Hi, how are you?" might be tokenized into ['Hi', ',', 'how', 'are', 'you', '?']. This step is crucial for preparing the text for the model to correctly interpret and process it.

KeyBERT:
KeyBERT is used to extract meaningful keywords and terms from text data. This tool helps identify the most relevant keywords and phrases in the text, which enhances the accuracy of search and recommendation processes. KeyBERT uses a BERT-based approach to extract key terms from the text, allowing for a better understanding of the main topics. For instance, it can identify keywords like "artificial intelligence" and "machine learning" from a paragraph, facilitating the provision of more specific answers related to these terms.

FAISS (Facebook AI Similarity Search):
FAISS is used for fast and efficient similarity searches of high-dimensional vectors. High-dimensional vectors typically represent text embeddings, and FAISS allows for rapid nearest neighbor searches among these vectors. In this project, FAISS is used to find the most relevant answers by searching for similarities between the vector representation of a user query and the vectors of previously answered questions. FAISS enables effective and quick search results, providing users with fast and accurate responses.

