#https://bab2min.github.io/tomotopy/v0.12.2/en/
import tomotopy as tp
from nltk.corpus import stopwords
import re
import csv

def tokenizer(doc,sw):
#     return [word for word in [re.sub('[^a-z]','',x.lower()) for x in doc.strip().split()]
#             if word not in sw and len(word)>2]
    s=doc[:doc.rindex(' ')].split(' ')
    r=[]
    for v in s:
        if v not in sw and len(v)>2:r.append(v)
    print(r)

sw=stopwords.words('english')

mdl = tp.CTModel(k=20)

with open( 'hotelreviews.csv') as f:
    for doc in f:
        mdl.add_doc(tokenizer(doc,sw))
#         tokenizer(doc,sw)

# for i in range(0, 500,100):
#     mdl.train(10)
    
# fw=open('topic.csv','w',encoding='utf8')
# writer=csv.writer(fw,lineterminator='\n')

# for k in range(mdl.k):
#     topk_words=[pair[0] for pair in mdl.get_topic_words(k, top_n=15)]
#     print(k,topk_words)
#     writer.writerow(','.join(topk_words))
#     print()

# fw=open('topic.csv','w',encoding='utf8')
# writer=csv.writer(fw,lineterminator='\n')
# for v in range(len(topk_words)):
#     print(topk_words[v].split(','))

