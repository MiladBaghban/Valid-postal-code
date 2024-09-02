import re

def validate_postal_code(postal_code):
    pattern = r'^\d{10}$'
    if re.match(pattern, postal_code):
        return True
    else:
        return False

def filter_valid_postal_codes(postal_codes):
    valid_postal_codes = []
    for code in postal_codes:
        if validate_postal_code(code):
            valid_postal_codes.append(code)
    return valid_postal_codes

user_input = ["5649821456", "0226540783", "fjyldmblrpl", "54321", "fksnt457dk"]
valid_codes = filter_valid_postal_codes(user_input)
print("valid_codes:", valid_codes)
