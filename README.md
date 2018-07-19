Repository for developing codes to data mine NIST ISODB

#be sure to only search piece1, piece2, and piece3 in lowercase!
def synonym_search(piece1, piece2, piece3):
    for synonym in synonyms:
        name = synonym.lower()
        if piece1 in name or piece2 in name:
            pieces_of_name = re.split(r'\W+', name)
            #print(pieces_of_name)
            for word in pieces_of_name:
                if word == piece3:
                    print(synonym)
